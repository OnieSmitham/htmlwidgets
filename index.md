---
title: "htmlwidgets for R"
---

<!--html_preserve-->

</div> <!--page-body-->
</div> <!--container-fluid main-container-->

<style type="text/css">
  .jumbotron {
    margin-top: 0;
  }
  .benefits {
    z-index: 1;
  }
  .benefits h4 {
    font-weight: 600;
    font-size: 22px;
  }
  .benefits ul {
    padding-left: 0;
    list-style: none outside none;
    margin-bottom: 24px;
    font-weight: 200;
    font-size: 18px;
  }
  .benefits li {
    margin-bottom: 12px;
  }
  .benefits li strong {
    font-weight: 400;
  }

  img.main-screenshot {
    position: relative;
    width: 100%;
  }
  #widget-carousel {
    box-shadow: 0 10px 30px 6px #BBB;
  }

  .showcase-teaser img {
    width: 100%;
    border: 1px solid #CCC;
    margin-bottom: 16px;
  }
  .below-lead h3 {
    margin-top: 24pt;
  }
  .below-lead h3:first-child {
    margin-top: 0;
  }
  .below-lead p {
    font-size: 14pt;
    font-weight: 200;
  }

  .pagination {
    display: table;
    margin: 0 auto;
    z-index: 1;
  }
  .pagination>li>a {
    display: inline-block;
    color: #333 !important;
    padding: 2px 0;
    margin-left: 12px !important;
    margin-right: 12px !important;
    background-color: transparent !important;
    border-color: transparent !important;
    text-shadow: 1px 1px 3px rgba(140, 140, 140, 0.2);
  }
  .pagination>li>a .bullet {
    display: block;
    width: 100%;
    text-align: center;
    visibility: hidden;
    color: #676767;
  }
  .pagination>li.active>a .bullet {
    visibility: visible;
  }
</style>
<script>
$(document).on("slide.bs.carousel", "#widget-carousel", function(e) {
  $(".pagination li.active").removeClass("active");
  var i = +$(e.relatedTarget).data("slide");
  $($(".pagination li")[i]).addClass("active");
});
</script>

<div class="jumbotron">
  <div class="container-fluid main-container">
    <div class="row">

      <div class="col-sm-5 benefits">
        <div class="hidden-xs">&nbsp;</div>
        <h4>Bring the best of JavaScript data visualization to R</h4>
        <ul>
          <li>Use JavaScript visualization libraries <strong>at the R console</strong>, just like plots</li>
          <li>Embed widgets in <strong>R Markdown</strong> documents and <strong>Shiny</strong> web applications</li>
          <li><strong>Develop new widgets</strong> using a framework that seamlessly bridges R and JavaScript</li>
        </ul>
      </div>

      <div class="col-sm-7">
        <div id="widget-carousel" class="carousel slide" data-ride="carousel" data-pause="">
          <!-- Indicators -->
          <ol class="carousel-indicators hide">
            <li data-target="#widget-carousel" data-slide-to="0" class="active"></li>
            <li data-target="#widget-carousel" data-slide-to="1"></li>
            <li data-target="#widget-carousel" data-slide-to="2"></li>
          </ol>

          <!-- Wrapper for slides -->
          <div class="carousel-inner" role="listbox">
            <div class="item active" data-slide="0">
              <img class="main-screenshot" src="images/rconsole.2x.png">
              <div class="carousel-caption">
              </div>
            </div>
            <div class="item" data-slide="1">
              <img src="images/rmarkdown.2x.png">
              <div class="carousel-caption">
              </div>
            </div>
            <div class="item" data-slide="2">
              <img src="images/shiny.2x.jpg">
              <div class="carousel-caption">
              </div>
            </div>
          </div>

          <!-- Controls -->
          <!--
          <a class="left carousel-control" href="#widget-carousel" role="button" data-slide="prev">
            <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
          </a>
          <a class="right carousel-control" href="#widget-carousel" role="button" data-slide="next">
            <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
          </a>
          -->
        </div>

        <ul class="pagination pagination-sm">
          <li class="active"><a href="javascript:void" data-target="#widget-carousel" data-slide-to="0"><span class="bullet">&#x25bc;</span>At the R console</a></li>
          <li><a href="javascript:void" data-target="#widget-carousel" data-slide-to="1"><span class="bullet">&#x25bc;</span>In R Markdown docs</a></li>
          <li><a href="javascript:void" data-target="#widget-carousel" data-slide-to="2"><span class="bullet">&#x25bc;</span>In Shiny apps</a></li>
        </ul>

      </div>


    </div> <!-- row -->
  </div> <!-- container-fluid main-container -->
</div> <!-- jumbotron -->

<div class="container-fluid main-container below-lead">
  <h3>Widgets in action</h3>
  <div class="row">
    <div class="col-sm-9">
      <div class="row showcase-teaser">
        <div class="col-xs-6 col-sm-3">
          <a href="showcase_leaflet.html"><img src="images/carousel-leaflet.png"/></a>
        </div>
        <div class="col-xs-6 col-sm-3">
          <a href="showcase_dygraphs.html"><img src="images/carousel-dygraphs.png"/></a>
        </div>
        <div class="col-xs-6 col-sm-3">
          <a href="showcase_networkD3.html"><img src="images/carousel-networkD3.png"/></a>
        </div>
        <div class="col-xs-6 col-sm-3">
          <a href="showcase_threejs.html"><img src="images/carousel-threejs.png"/></a>
        </div>
      </div>
    </div>
  </div>
  <div class="row">
    <div class="col-sm-9">
      <p>Just a line or two of R code can be used to create interactive visualizations. See the featured widgets in the <a href="showcase_leaflet.html">showcase</a> and browse over 50 available widgets in the <a href="http://gallery.htmlwidgets.org">gallery</a>.</p>
    </div>
    <div class="col-sm-3">
      <p><a class="btn btn-info" href="showcase_leaflet.html" role="button">See the showcase &raquo;</a></p>
    </div>
  </div>
  <hr/>
  
  
  <h3>Interactive dashboards</h3>
  <div class="row">
    <div class="col-sm-9">
      <div class="row showcase-teaser" style="display: none;">
        <div class="col-xs-6 col-sm-3">
          <a href="https://beta.rstudioconnect.com/jjallaire/htmlwidgets-showcase-storyboard/htmlwidgets-showcase-storyboard.html"><img src="http://rmarkdown.rstudio.com/flexdashboard/images/htmlwidgets-showcase-storyboard.png"/></a>
        </div>
        <div class="col-xs-6 col-sm-3">
          <a href="https://beta.rstudioconnect.com/jjallaire/htmlwidgets-d3heatmap/htmlwidgets-d3heatmap.html"><img src="http://rmarkdown.rstudio.com/flexdashboard/images/htmlwidgets-d3heatmap.png"/></a>
        </div>
       
        <div class="col-xs-6 col-sm-3">
          <a href="https://beta.rstudioconnect.com/jjallaire/htmlwidgets-metricsgraphics-tor/htmlwidgets-metricsgraphics-tor.html"><img src="http://rmarkdown.rstudio.com/flexdashboard/images/htmlwidgets-metricsgraphics-tor.png"/></a>
        </div>
        <div class="col-xs-6 col-sm-3">
          <a href="http://jkunst.com/flexdashboard-highcharter-examples/pokemon/"><img src="http://rmarkdown.rstudio.com/flexdashboard/images/highcharter-pokemon.png"/></a>
        </div>
      </div>
    </div>
  </div>
  <div class="row">
    <div class="col-sm-9">
      <p>You can easily compose multiple htmlwidgets into a dashboard using the <a href="http://rmarkdown.rstudio.com/flexdashboard">flexdashboard</a> package, which features flexible and easy to specify row and column-based layouts for multiple widgets.</p>
    </div>
    <div class="col-sm-3">
      <p><a class="btn btn-success" href="http://rmarkdown.rstudio.com/flexdashboard/" role="button">Create a dashboard &raquo;</a></p>
    </div>
  </div>
  <hr/>
  
  
  <h3>Widgets in harmony</h3>
  <div class="row">
    <div class="col-sm-9">
      <p>Widgets can be wired together using the <a href="https://rstudio.github.io/crosstalk">crosstalk</a> package. Linked brushing between widgets and client side filtering are currently supported. Use Shiny to create more sophisticated interactions.</p>
    </div>
    <div class="col-sm-3">
      <p><a class="btn btn-warning" href="develop_intro.html" role="button">Learn about crosstalk  &raquo;</a></p>
    </div>
  </div>
  
  <hr/>
  
  <h3>Creating widgets</h3>
  <div class="row">
    <div class="col-sm-9">
      <p>Learn how to create an R binding for your favorite JavaScript library and enable use of it in the R console, in R Markdown documents, and in Shiny web applications.</p>
    </div>
    <div class="col-sm-3">
      <p><a class="btn btn-primary" href="develop_intro.html" role="button">Develop a widget &raquo;</a></p>
    </div>
  </div>
</div>

<!--/html_preserve-->
