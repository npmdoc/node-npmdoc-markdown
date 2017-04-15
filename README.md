# api documentation for  [markdown (v0.5.0)](https://github.com/evilstreak/markdown-js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-markdown.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-markdown) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-markdown.svg)](https://travis-ci.org/npmdoc/node-npmdoc-markdown)
#### A sensible Markdown parser for javascript

[![NPM](https://nodei.co/npm/markdown.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/markdown)

[![apidoc](https://npmdoc.github.io/node-npmdoc-markdown/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-markdown/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-markdown/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-markdown/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "md2html": "./bin/md2html.js"
    },
    "bugs": {
        "url": "http://github.com/evilstreak/markdown-js/issues"
    },
    "contributors": [
        {
            "name": "Dominic Baggott",
            "url": "http://evilstreak.co.uk"
        },
        {
            "name": "Ash Berlin",
            "url": "http://ashberlin.com"
        }
    ],
    "dependencies": {
        "nopt": "~2.1.1"
    },
    "description": "A sensible Markdown parser for javascript",
    "devDependencies": {
        "tap": "~0.3.3"
    },
    "directories": {},
    "dist": {
        "shasum": "28205b565a8ae7592de207463d6637dc182722b2",
        "tarball": "https://registry.npmjs.org/markdown/-/markdown-0.5.0.tgz"
    },
    "engines": {
        "node": "*"
    },
    "homepage": "https://github.com/evilstreak/markdown-js#readme",
    "keywords": [
        "markdown",
        "text processing",
        "ast"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "http://www.opensource.org/licenses/mit-license.php"
        }
    ],
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "ashb"
        },
        {
            "name": "dom"
        }
    ],
    "name": "markdown",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/evilstreak/markdown-js.git"
    },
    "scripts": {
        "test": "tap ./test/*.t.js"
    },
    "version": "0.5.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module markdown](#apidoc.module.markdown)
1.  [function <span class="apidocSignatureSpan">markdown.</span>markdown.Markdown (dialect)](#apidoc.element.markdown.markdown.Markdown)
1.  [function <span class="apidocSignatureSpan">markdown.</span>parse ( source , dialect , options )](#apidoc.element.markdown.parse)
1.  object <span class="apidocSignatureSpan"></span>markdown
1.  object <span class="apidocSignatureSpan">markdown.</span>markdown.Markdown.prototype

#### [module markdown.markdown](#apidoc.module.markdown.markdown)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.</span>Markdown (dialect)](#apidoc.element.markdown.markdown.Markdown)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.</span>parse ( source, dialect )](#apidoc.element.markdown.markdown.parse)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.</span>renderJsonML ( jsonml, options )](#apidoc.element.markdown.markdown.renderJsonML)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.</span>toHTML ( source , dialect , options )](#apidoc.element.markdown.markdown.toHTML)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.</span>toHTMLTree ( input, dialect , options )](#apidoc.element.markdown.markdown.toHTMLTree)

#### [module markdown.markdown.Markdown](#apidoc.module.markdown.markdown.Markdown)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.</span>Markdown (dialect)](#apidoc.element.markdown.markdown.Markdown.Markdown)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>buildBlockOrder (d)](#apidoc.element.markdown.markdown.Markdown.buildBlockOrder)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>buildInlinePatterns (d)](#apidoc.element.markdown.markdown.Markdown.buildInlinePatterns)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>mk_block (block, trail, line)](#apidoc.element.markdown.markdown.Markdown.mk_block)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>subclassDialect ( d )](#apidoc.element.markdown.markdown.Markdown.subclassDialect)
1.  object <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>DialectHelpers
1.  object <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>dialects

#### [module markdown.markdown.Markdown.prototype](#apidoc.module.markdown.markdown.Markdown.prototype)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>debug ()](#apidoc.element.markdown.markdown.Markdown.prototype.debug)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>loop_re_over_block ( re, block, cb )](#apidoc.element.markdown.markdown.Markdown.prototype.loop_re_over_block)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>processBlock ( block, next )](#apidoc.element.markdown.markdown.Markdown.prototype.processBlock)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>processInline ( block )](#apidoc.element.markdown.markdown.Markdown.prototype.processInline)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>split_blocks ( input, startLine )](#apidoc.element.markdown.markdown.Markdown.prototype.split_blocks)
1.  [function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>toTree ( source, custom_root )](#apidoc.element.markdown.markdown.Markdown.prototype.toTree)



# <a name="apidoc.module.markdown"></a>[module markdown](#apidoc.module.markdown)

#### <a name="apidoc.element.markdown.markdown.Markdown"></a>[function <span class="apidocSignatureSpan">markdown.</span>markdown.Markdown (dialect)](#apidoc.element.markdown.markdown.Markdown)
- description and source-code
```javascript
markdown.Markdown = function (dialect) {
  switch (typeof dialect) {
    case "undefined":
      this.dialect = Markdown.dialects.Gruber;
      break;
    case "object":
      this.dialect = dialect;
      break;
    default:
      if ( dialect in Markdown.dialects ) {
        this.dialect = Markdown.dialects[dialect];
      }
      else {
        throw new Error("Unknown Markdown dialect '" + String(dialect) + "'");
      }
      break;
  }
  this.em_state = [];
  this.strong_state = [];
  this.debug_indent = "";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.parse"></a>[function <span class="apidocSignatureSpan">markdown.</span>parse ( source , dialect , options )](#apidoc.element.markdown.parse)
- description and source-code
```javascript
function toHTML( source , dialect , options ) {
  var input = expose.toHTMLTree( source , dialect , options );

  return expose.renderJsonML( input );
}
```
- example usage
```shell
...
'''js
var md = require( "markdown" ).markdown,
  text = "[Markdown] is a simple text-based [markup language]\n" +
         "created by [John Gruber]\n\n" +
         "[John Gruber]: http://daringfireball.net";

// parse the markdown into a tree and grab the link references
var tree = md.parse( text ),
  refs = tree[ 1 ].references;

// iterate through the tree finding link references
( function find_link_refs( jsonml ) {
if ( jsonml[ 0 ] === "link_ref" ) {
  var ref = jsonml[ 1 ].ref;
...
```



# <a name="apidoc.module.markdown.markdown"></a>[module markdown.markdown](#apidoc.module.markdown.markdown)

#### <a name="apidoc.element.markdown.markdown.Markdown"></a>[function <span class="apidocSignatureSpan">markdown.markdown.</span>Markdown (dialect)](#apidoc.element.markdown.markdown.Markdown)
- description and source-code
```javascript
Markdown = function (dialect) {
  switch (typeof dialect) {
    case "undefined":
      this.dialect = Markdown.dialects.Gruber;
      break;
    case "object":
      this.dialect = dialect;
      break;
    default:
      if ( dialect in Markdown.dialects ) {
        this.dialect = Markdown.dialects[dialect];
      }
      else {
        throw new Error("Unknown Markdown dialect '" + String(dialect) + "'");
      }
      break;
  }
  this.em_state = [];
  this.strong_state = [];
  this.debug_indent = "";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.parse"></a>[function <span class="apidocSignatureSpan">markdown.markdown.</span>parse ( source, dialect )](#apidoc.element.markdown.markdown.parse)
- description and source-code
```javascript
parse = function ( source, dialect ) {
  // dialect will default if undefined
  var md = new Markdown( dialect );
  return md.toTree( source );
}
```
- example usage
```shell
...
'''js
var md = require( "markdown" ).markdown,
  text = "[Markdown] is a simple text-based [markup language]\n" +
         "created by [John Gruber]\n\n" +
         "[John Gruber]: http://daringfireball.net";

// parse the markdown into a tree and grab the link references
var tree = md.parse( text ),
  refs = tree[ 1 ].references;

// iterate through the tree finding link references
( function find_link_refs( jsonml ) {
if ( jsonml[ 0 ] === "link_ref" ) {
  var ref = jsonml[ 1 ].ref;
...
```

#### <a name="apidoc.element.markdown.markdown.renderJsonML"></a>[function <span class="apidocSignatureSpan">markdown.markdown.</span>renderJsonML ( jsonml, options )](#apidoc.element.markdown.markdown.renderJsonML)
- description and source-code
```javascript
renderJsonML = function ( jsonml, options ) {
  options = options || {};
  // include the root element in the rendered output?
  options.root = options.root || false;

  var content = [];

  if ( options.root ) {
    content.push( render_tree( jsonml ) );
  }
  else {
    jsonml.shift(); // get rid of the tag
    if ( jsonml.length && typeof jsonml[ 0 ] === "object" && !( jsonml[ 0 ] instanceof Array ) ) {
      jsonml.shift(); // get rid of the attributes
    }

    while ( jsonml.length ) {
      content.push( render_tree( jsonml.shift() ) );
    }
  }

  return content.join( "\n\n" );
}
```
- example usage
```shell
...
  }
  else if ( Array.isArray( jsonml[ 2 ] ) ) {
    jsonml[ 2 ].forEach( find_link_refs );
  }
} )( tree );

// convert the tree into html
var html = md.renderJsonML( md.toHTMLTree( tree ) );
console.log( html );
'''

## Intermediate Representation

Internally the process to convert a chunk of markdown into a chunk of
HTML has three steps:
...
```

#### <a name="apidoc.element.markdown.markdown.toHTML"></a>[function <span class="apidocSignatureSpan">markdown.markdown.</span>toHTML ( source , dialect , options )](#apidoc.element.markdown.markdown.toHTML)
- description and source-code
```javascript
function toHTML( source , dialect , options ) {
  var input = expose.toHTMLTree( source , dialect , options );

  return expose.renderJsonML( input );
}
```
- example usage
```shell
...

### Node

The simple way to use it with node is:

'''js
var markdown = require( "markdown" ).markdown;
console.log( markdown.toHTML( "Hello *World*!" ) );
'''

### Browser

It also works in a browser; here is a complete example:

'''html
...
```

#### <a name="apidoc.element.markdown.markdown.toHTMLTree"></a>[function <span class="apidocSignatureSpan">markdown.markdown.</span>toHTMLTree ( input, dialect , options )](#apidoc.element.markdown.markdown.toHTMLTree)
- description and source-code
```javascript
function toHTMLTree( input, dialect , options ) {
  // convert string input to an MD tree
  if ( typeof input ==="string" ) input = this.parse( input, dialect );

  // Now convert the MD tree to an HTML tree

  // remove references from the tree
  var attrs = extract_attr( input ),
      refs = {};

  if ( attrs && attrs.references ) {
    refs = attrs.references;
  }

  var html = convert_tree_to_html( input, refs , options );
  merge_text_nodes( html );
  return html;
}
```
- example usage
```shell
...
  }
  else if ( Array.isArray( jsonml[ 2 ] ) ) {
    jsonml[ 2 ].forEach( find_link_refs );
  }
} )( tree );

// convert the tree into html
var html = md.renderJsonML( md.toHTMLTree( tree ) );
console.log( html );
'''

## Intermediate Representation

Internally the process to convert a chunk of markdown into a chunk of
HTML has three steps:
...
```



# <a name="apidoc.module.markdown.markdown.Markdown"></a>[module markdown.markdown.Markdown](#apidoc.module.markdown.markdown.Markdown)

#### <a name="apidoc.element.markdown.markdown.Markdown.Markdown"></a>[function <span class="apidocSignatureSpan">markdown.markdown.</span>Markdown (dialect)](#apidoc.element.markdown.markdown.Markdown.Markdown)
- description and source-code
```javascript
Markdown = function (dialect) {
  switch (typeof dialect) {
    case "undefined":
      this.dialect = Markdown.dialects.Gruber;
      break;
    case "object":
      this.dialect = dialect;
      break;
    default:
      if ( dialect in Markdown.dialects ) {
        this.dialect = Markdown.dialects[dialect];
      }
      else {
        throw new Error("Unknown Markdown dialect '" + String(dialect) + "'");
      }
      break;
  }
  this.em_state = [];
  this.strong_state = [];
  this.debug_indent = "";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.buildBlockOrder"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>buildBlockOrder (d)](#apidoc.element.markdown.markdown.Markdown.buildBlockOrder)
- description and source-code
```javascript
buildBlockOrder = function (d) {
  var ord = [];
  for ( var i in d ) {
    if ( i == "__order__" || i == "__call__" ) continue;
    ord.push( i );
  }
  d.__order__ = ord;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.buildInlinePatterns"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>buildInlinePatterns (d)](#apidoc.element.markdown.markdown.Markdown.buildInlinePatterns)
- description and source-code
```javascript
buildInlinePatterns = function (d) {
  var patterns = [];

  for ( var i in d ) {
    // __foo__ is reserved and not a pattern
    if ( i.match( /^__.*__$/) ) continue;
    var l = i.replace( /([\\.*+?|()\[\]{}])/g, "\\$1" )
             .replace( /\n/, "\\n" );
    patterns.push( i.length == 1 ? l : "(?:" + l + ")" );
  }

  patterns = patterns.join("|");
  d.__patterns__ = patterns;
  //print("patterns:", uneval( patterns ) );

  var fn = d.__call__;
  d.__call__ = function(text, pattern) {
    if ( pattern != undefined ) {
      return fn.call(this, text, pattern);
    }
    else
    {
      return fn.call(this, text, patterns);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.mk_block"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>mk_block (block, trail, line)](#apidoc.element.markdown.markdown.Markdown.mk_block)
- description and source-code
```javascript
mk_block = function (block, trail, line) {
  // Be helpful for default case in tests.
  if ( arguments.length == 1 ) trail = "\n\n";

  var s = new String(block);
  s.trailing = trail;
  // To make it clear its not just a string
  s.inspect = mk_block_inspect;
  s.toSource = mk_block_toSource;

  if ( line != undefined )
    s.lineNumber = line;

  return s;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.subclassDialect"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.</span>subclassDialect ( d )](#apidoc.element.markdown.markdown.Markdown.subclassDialect)
- description and source-code
```javascript
subclassDialect = function ( d ) {
  function Block() {}
  Block.prototype = d.block;
  function Inline() {}
  Inline.prototype = d.inline;

  return { block: new Block(), inline: new Inline() };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.markdown.markdown.Markdown.prototype"></a>[module markdown.markdown.Markdown.prototype](#apidoc.module.markdown.markdown.Markdown.prototype)

#### <a name="apidoc.element.markdown.markdown.Markdown.prototype.debug"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>debug ()](#apidoc.element.markdown.markdown.Markdown.prototype.debug)
- description and source-code
```javascript
debug = function () {
  var args = Array.prototype.slice.call( arguments);
  args.unshift(this.debug_indent);
  if ( typeof print !== "undefined" )
      print.apply( print, args );
  if ( typeof console !== "undefined" && typeof console.log !== "undefined" )
      console.log.apply( null, args );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.prototype.loop_re_over_block"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>loop_re_over_block ( re, block, cb )](#apidoc.element.markdown.markdown.Markdown.prototype.loop_re_over_block)
- description and source-code
```javascript
loop_re_over_block = function ( re, block, cb ) {
  // Dont use /g regexps with this
  var m,
      b = block.valueOf();

  while ( b.length && (m = re.exec(b) ) != null ) {
    b = b.substr( m[0].length );
    cb.call(this, m);
  }
  return b;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.prototype.processBlock"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>processBlock ( block, next )](#apidoc.element.markdown.markdown.Markdown.prototype.processBlock)
- description and source-code
```javascript
function processBlock( block, next ) {
  var cbs = this.dialect.block,
      ord = cbs.__order__;

  if ( "__call__" in cbs ) {
    return cbs.__call__.call(this, block, next);
  }

  for ( var i = 0; i < ord.length; i++ ) {
    //D:this.debug( "Testing", ord[i] );
    var res = cbs[ ord[i] ].call( this, block, next );
    if ( res ) {
      //D:this.debug("  matched");
      if ( !isArray(res) || ( res.length > 0 && !( isArray(res[0]) ) ) )
        this.debug(ord[i], "didn't return a proper array");
      //D:this.debug( "" );
      return res;
    }
  }

  // Uhoh! no match! Should we throw an error?
  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.prototype.processInline"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>processInline ( block )](#apidoc.element.markdown.markdown.Markdown.prototype.processInline)
- description and source-code
```javascript
function processInline( block ) {
  return this.dialect.inline.__call__.call( this, String( block ) );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.prototype.split_blocks"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>split_blocks ( input, startLine )](#apidoc.element.markdown.markdown.Markdown.prototype.split_blocks)
- description and source-code
```javascript
function splitBlocks( input, startLine ) {
  input = input.replace(/(\r\n|\n|\r)/g, "\n");
  // [\s\S] matches _anything_ (newline or space)
  // [^] is equivalent but doesn't work in IEs.
  var re = /([\s\S]+?)($|\n#|\n(?:\s*\n|$)+)/g,
      blocks = [],
      m;

  var line_no = 1;

  if ( ( m = /^(\s*\n)/.exec(input) ) != null ) {
    // skip (but count) leading blank lines
    line_no += count_lines( m[0] );
    re.lastIndex = m[0].length;
  }

  while ( ( m = re.exec(input) ) !== null ) {
    if (m[2] == "\n#") {
      m[2] = "\n";
      re.lastIndex--;
    }
    blocks.push( mk_block( m[1], m[2], line_no ) );
    line_no += count_lines( m[0] );
  }

  return blocks;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.markdown.markdown.Markdown.prototype.toTree"></a>[function <span class="apidocSignatureSpan">markdown.markdown.Markdown.prototype.</span>toTree ( source, custom_root )](#apidoc.element.markdown.markdown.Markdown.prototype.toTree)
- description and source-code
```javascript
function toTree( source, custom_root ) {
  var blocks = source instanceof Array ? source : this.split_blocks( source );

  // Make tree a member variable so its easier to mess with in extensions
  var old_tree = this.tree;
  try {
    this.tree = custom_root || this.tree || [ "markdown" ];

    blocks:
    while ( blocks.length ) {
      var b = this.processBlock( blocks.shift(), blocks );

      // Reference blocks and the like won't return any content
      if ( !b.length ) continue blocks;

      this.tree.push.apply( this.tree, b );
    }
    return this.tree;
  }
  finally {
    if ( custom_root ) {
      this.tree = old_tree;
    }
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
