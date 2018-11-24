```
21. HTMLPurifier – HTML XSS 防护

HTMLPurifier是一个HTML过滤库，通过强大的白名单和聚集分析，保护你代码远离XSS攻击。它也确保输出标记符合标准。 (源码在github上)

require_once '/path/to/HTMLPurifier.auto.php';
$config = HTMLPurifier_Config::createDefault();
$purifier = new HTMLPurifier($config);
$clean_html = $purifier->purify($dirty_html);
如果你的网站允许用户提交 HTML 代码，不修改就展示代码的话，那这时候就是用这个库的时候了。


```
HTML Purifier [![Build Status](https://secure.travis-ci.org/ezyang/htmlpurifier.svg?branch=master)](http://travis-ci.org/ezyang/htmlpurifier)
=============

HTML Purifier is an HTML filtering solution that uses a unique combination
of robust whitelists and aggressive parsing to ensure that not only are
XSS attacks thwarted, but the resulting HTML is standards compliant.

HTML Purifier is oriented towards richly formatted documents from
untrusted sources that require CSS and a full tag-set.  This library can
be configured to accept a more restrictive set of tags, but it won't be
as efficient as more bare-bones parsers. It will, however, do the job
right, which may be more important.

Places to go:

* See INSTALL for a quick installation guide
* See docs/ for developer-oriented documentation, code examples and
  an in-depth installation guide.
* See WYSIWYG for information on editors like TinyMCE and FCKeditor

HTML Purifier can be found on the web at: [http://htmlpurifier.org/](http://htmlpurifier.org/)

## Installation

Package available on [Composer](https://packagist.org/packages/ezyang/htmlpurifier).

If you're using Composer to manage dependencies, you can use

    $ composer require ezyang/htmlpurifier
