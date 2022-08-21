---
title: CSSStyleDeclaration.getPropertyPriority()
slug: Web/API/CSSStyleDeclaration/getPropertyPriority
tags:
- API
- CSSOM
- Method
- Reference
browser-compat: api.CSSStyleDeclaration.getPropertyPriority
translation_of: Web/API/CSSStyleDeclaration/getPropertyPriority
---
<p>{{ APIRef("CSSOM") }}</p>

<p><strong>CSSStyleDeclaration.getPropertyPriority()</strong> メソッドインターフェイスは、 {{domxref('DOMString')}} でその CSS プロパティに明示的に設定されたすべての優先度を返します。</p>

<h2 id="Syntax">構文</h2>

<pre
  class="brush: js">var <em>priority</em> = <em>style</em>.getPropertyPriority(<em>property</em>);</pre>

<h3 id="Parameters">引数</h3>

<ul>
  <li><em><code>property</code></em> は {{domxref('DOMString')}} で、チェックするプロパティ名を表します。</li>
</ul>

<h3 id="Return_value">返値</h3>

<ul>
  <li><code><em>priority</em></code> は {{domxref('DOMString')}} で、存在する場合は優先度 (<code>"important"</code> など) を表します。存在しない場合は、空文字列を返します。</li>
</ul>

<h2 id="Example">例</h2>

<p>以下の JavaScript コードは、 <code>margin</code> が CSS セレクターの規則で important と記されているかどうかをチェックします。</p>

<pre class="brush: js">var declaration = document.styleSheets[0].cssRules[0].style;
var isImportant = declaration.getPropertyPriority('margin') === 'important';
</pre>

<h2 id="Specifications">仕様書</h2>

{{Specifications}}

<h2 id="Browser_compatibility">ブラウザーの互換性</h2>

<p>{{Compat}}</p>