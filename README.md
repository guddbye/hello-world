<!doctype html>
<title>CSS Grid Template 1</title>
<style>
body { 
  display: grid;
  grid-template-areas: 
    "header header header"
    "nav article ads"
    "nav footer footer";
  grid-template-rows: 80px 1fr 70px;  
  grid-template-columns: 20% 1fr 15%;
  grid-row-gap: 10px;
  grid-column-gap: 10px;
  height: 100vh;
  margin: 0;
  }  
header, footer, article, nav, div {
  padding: 1.2em;
  background: gold;
  }
#pageHeader {
  grid-area: header;
  }
#pageFooter {
  grid-area: footer;
  }
#mainArticle { 
  grid-area: article;      
  }
#mainNav { 
  grid-area: nav; 
  }
#siteAds { 
  grid-area: ads; 
  } 
/* Stack the layout on small devices/viewports. */
@media all and (max-width: 575px) {
  body { 
    grid-template-areas: 
      "header"
      "article"
      "ads"
      "nav"
      "footer";
    grid-template-rows: 80px 1fr 70px 1fr 70px;  
    grid-template-columns: 1fr;
 }
}
</style>
<body>
  <header id="pageHeader">Gunther's Corner</header>
  <article id="mainArticle">Catalog</article>
  <nav id="mainNav">Right Menu</nav>
  <div id="siteAds">Left Menu</div>
    <footer id="pageFooter"><p>&copy;</p> Gunter's Corner</footer>
</body>
