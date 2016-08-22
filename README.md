# Typedoc-Webpack-Plugin
This is a plugin for the Webpack build system that will run Typedoc in order to generate API documentation.

To use, add a require for the module to the Webpack Configuration file, and then place into plugin section:


```
var TypedocWebpackPlugin = require('typedoc-webpack-plugin');

...

plugins: [
	new TypedocWebpackPlugin({
		out: './target/docs',
		target: 'es5',
		mode: 'file',
		exclude: '**/node_modules/**/*.*',
		theme: './typedoc-theme/',
		includeDeclarations: false,
		experimentalDecorators: true,
		ignoreCompilerErrors: true,
		excludeExternals: true,
		module: 'commonjs',
		name: 'Contoso'
	})
]
```


The options for the plugin mirror the options that are passed to typedoc. Refer to https://github.com/TypeStrong/typedoc for full options. 

The default options that are set by the plugin are:

```
{
	out: './docs',
	module: 'commonjs',
	target: 'es5',
	exclude: '**/node_modules/**/*.*',
	experimentalDecorators: true,
	excludeExternals: true
}
```