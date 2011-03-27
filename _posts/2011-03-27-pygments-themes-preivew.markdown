---
layout: post
title: Pygments Themes Preview
stylesheet: themes.css
---

<script type="text/javascript" charset="utf-8">
  function setTheme(select) {
    var theme = select.options[select.selectedIndex].text;
    document.getElementById("code").className = theme;
  }  	  
</script>

<select id="theme" onchange="setTheme(this);">
  <option>autumn</option>
  <option>borland</option>
  <option>bw</option>
  <option>colorful</option>
  <option>default</option>
  <option>emacs</option>
  <option>friendly</option>
  <option>fruity</option>
  <option>manni</option>
  <option>murphy</option>
  <option>native</option>
  <option>pastie</option>
  <option>perldoc</option>
  <option>tango</option>
  <option>trac</option>
  <option>vim</option>
  <option>vs</option>
  <option>railscasts</option>
</select>

<div id="code" class="autumn">

<div class="pygments"><pre><code class="ruby"><span class="c1"># simple proxy</span>
<span class="k">class</span> <span class="nc">Proxy</span>
  <span class="k">def</span> <span class="nf">initialize</span><span class="p">(</span><span class="n">target</span><span class="p">)</span>
    <span class="vi">@target</span> <span class="o">=</span> <span class="n">target</span>
  <span class="k">end</span>

  <span class="k">def</span> <span class="nf">method_missing</span><span class="p">(</span><span class="nb">name</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">&amp;</span><span class="n">block</span><span class="p">)</span>
    <span class="nb">puts</span> <span class="s2">&quot;proxying </span><span class="si">#{</span><span class="nb">name</span><span class="si">}</span><span class="s2">&quot;</span>
    <span class="vi">@target</span><span class="o">.</span><span class="n">send</span><span class="p">(</span><span class="nb">name</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">&amp;</span><span class="n">block</span><span class="p">)</span>
  <span class="k">end</span>
<span class="k">end</span>
</code></pre></div>

<div class="pygments"><pre><code class="html"><span class="cp">&lt;!DOCTYPE html&gt;</span>
<span class="nt">&lt;html</span> <span class="na">lang=</span><span class="s">&quot;en&quot;</span><span class="nt">&gt;</span>
  <span class="nt">&lt;head&gt;</span>
    <span class="nt">&lt;title&gt;</span>Hello, world!<span class="nt">&lt;/title&gt;</span>
    <span class="nt">&lt;script&gt;</span>
      <span class="nx">jQuery</span><span class="p">(</span><span class="nb">document</span><span class="p">).</span><span class="nx">ready</span><span class="p">(</span><span class="kd">function</span><span class="p">(</span><span class="nx">$</span><span class="p">)</span> <span class="p">{</span>
        <span class="nx">$</span><span class="p">(</span><span class="s2">&quot;h1&quot;</span><span class="p">).</span><span class="nx">fadeIn</span><span class="p">(</span><span class="s2">&quot;slow&quot;</span><span class="p">);</span>
      <span class="p">});</span>
    <span class="nt">&lt;/script&gt;</span>
  <span class="nt">&lt;/head&gt;</span>
  <span class="nt">&lt;body&gt;</span>
    <span class="nt">&lt;h1&gt;</span>Hello, world!<span class="nt">&lt;/h1&gt;</span>
  <span class="nt">&lt;/body&gt;</span>
<span class="nt">&lt;/html&gt;</span>
</code></pre></div>

</div>
