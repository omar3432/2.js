# 2.js
&lt;![CDATA[*/ $(function(){$(window).one("scroll",function(){if(-1===window.location.href.indexOf("updated-min")){var e=$(".post-outer").length,n=0&lt;$(".index-author").length?!0:!1,p=$(".post-outer .ReadMore:first").text(),f,l=-1!==window.location.href.indexOf("/search/label/")?"/feeds/posts/summary/-/"+window.location.href.match(/\/label\/.+\?/)[0].replace(/\/label\//,"").replace("?",""):"/feeds/posts/summary";$.get(l+"?alt=json-in-script&amp;max-results=0",function(m){function b(){Math.ceil(f/e)>$(".nums").width()/ 40?0==$("#Pagination .pg-prev").length&amp;&amp;("rtl"===b_dir?$("#Pagination").prepend('&lt;a class="pg-prev">&amp;#xf101;&lt;/a>').append('&lt;a class="pg-next">&amp;#xf100;&lt;/a>'):$("#Pagination").prepend('&lt;a class="pg-prev">&amp;#xf100;&lt;/a>').append('&lt;a class="pg-next">&amp;#xf101;&lt;/a>')):$("#Pagination .pg-prev, #Pagination .pg-next").remove()}f=m.feed.openSearch$totalResults.$t;$("#Pagination .nums").prepend('&lt;span class="curr">1&lt;/span>');for(i=2;i&lt;=Math.ceil(f/e);i++)$("#Pagination .nums").append("&lt;span>"+i+"&lt;/span>");b(); $(window).resize(b);$("body").on("click",".pg-next",function(){$('.nums span:not(".hid-num"):first').text()!=Math.ceil(f/e)-Math.floor($(".nums").width()/40)+1&amp;&amp;$('.nums span:not(".hid-num"):first').addClass("hid-num")});$("body").on("click",".pg-prev",function(){$(".nums span.hid-num:last").removeAttr("class")})},"jsonp");$("body").on("click","#Pagination span:not(.curr)",function(){$(".curr").removeClass("curr");$(this).addClass("curr");$(".post-outer").addClass("opac");var f=$(this).text()*e-e+ 1;$.get(l+"?alt=json-in-script&amp;max-results="+e+"&amp;start-index="+f,function(b){$(".post-outer").remove();var a="",c,g;for(c=0;c&lt;b.feed.entry.length;c+=1){for(g=0;g&lt;b.feed.entry[c].link.length;g+=1){var h=b.feed.entry[c].link[g];if("alternate"==h.rel){var d=h.href;d=httpsEnabled?d.replace("http://","https://"):d;break}}g=b.feed.entry[c].summary.$t.replace(/&lt;\S[^>]*>/g,"");g=g.substr(0,100)+" ...";h=b.feed.entry[c].title.$t;var e=b.feed.entry[c].author[0].name.$t,f=void 0!==b.feed.entry[c].author[0].uri? b.feed.entry[c].author[0].uri.$t:"",l=b.feed.entry[c].published.$t,k=void 0!==b.feed.entry[c].media$thumbnail?b.feed.entry[c].media$thumbnail.url:alt_Img,m=ResizeImg(k,1600);k=-1!==k.indexOf("youtube.com/vi/")?k.replace("/default.","/hqdefault."):rct_cards?ResizeImg(k,t_index_cards[0],t_index_cards[1]):ResizeImg(k,t_index[0],t_index[1]);a=rct_cards?a+"&lt;div class='post-outer notr'>&lt;div class='rct-cards'>":a+"&lt;div class='post-outer notr'>&lt;div class='index-body'>";a+='&lt;a class="RecentThumb" href="'+ d+'" title="'+h+'">';a+='&lt;span style="background-image:url('+k+');">&lt;/span>';a+='&lt;div class="boxs">&lt;/div>&lt;/a>';a+='&lt;h2 class="post-title entry-title" itemprop="name headline">&lt;a href="'+d+'" title="'+h+'">'+h+"&lt;/a>&lt;/h2>";a+='&lt;div class="boxs">&lt;/div>&lt;/a>';a+='&lt;div class="details">';n&amp;&amp;(a+='&lt;span class="index-author" itemprop="author" itemscope="itemscope" itemtype="https://schema.org/Person">&lt;a class="fn g-profile" href="'+f+'" rel="author" title="author profile" data-gapiscan="true" data-onload="true" data-gapiattached="true">&lt;span itemprop="name">'+ e+'&lt;/span>&lt;/a>&lt;a class="url" href="" itemprop="url">&lt;/a>&lt;/span>');a+='&lt;span class="index-time">&lt;abbr class="timeago published updated" itemprop="datePublished dateModified" title="'+l+'">'+l+"&lt;/abbr>&lt;/span>&lt;/div>";a+='&lt;p class="RecentSnippet">'+g+"&lt;/p>";a+='&lt;a class="ReadMore" href="'+d+'" title="'+h+'">'+p+"&lt;/a>";a+='&lt;a class="ShareIndex fa fa-heart-o" title="Share Post">&lt;/a>&lt;div class="ShareIndexBut notr">';a+='&lt;a class="fb" href="https://www.facebook.com/sharer/sharer.php?u='+d+'" rel="noopener" target="_blank" title="Share">\uf09a&lt;/a>'; a+='&lt;a class="go" href="https://plus.google.com/share?url='+d+'" rel="noopener" target="_blank" title="+1">\uf1a0&lt;/a>';a+='&lt;a class="tw" href="https://twitter.com/home?status='+d+'" rel="noopener" target="_blank" title="Tweet">\uf099&lt;/a>';a+='&lt;a class="pin" href="https://pinterest.com/pin/create/button/?url'+d+"&amp;amp;media="+m+"&amp;amp;description="+h+'" rel="noopener" target="_blank" title="Pin It">\uf0d2&lt;/a>';a+="&lt;/div>&lt;/div>&lt;/div>"}$(".blog-posts").html(a+'&lt;i class="clear"/>');rct_cards&amp;&amp;(b=Math.round($(".blog-posts").outerWidth()/ 240),cards_width(b,20*b-20));$("html,body").stop().animate({scrollTop:$("#Blog1").offset().top});jQuery("abbr.timeago").timeago()},"jsonp")})}else $("#Pagination").remove()})}); /*]]>
