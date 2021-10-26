

```python
#Import required packages
import requests
import html5lib
from bs4 import BeautifulSoup
```


```python
url = "https://hec.ac.mw/scholarships"

res = requests.get(url)
```


```python
#print response
print(res.status_code)
```

    200
    


```python
#print text 
print(res.text)
```

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>Scholarship Opportunities | Higher Education Central Malawi</title>
        <meta name="description" content="">
        <meta name="title" content="">
        <meta name="author" content="HEC Media">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="generator" content="Higher Education Central Malawi">
    
        
        
        <link rel="icon" type="image/ico" href="https://hec.ac.mw/themes/hec/assets/images/favicon.ico">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/bootstrap.min.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/normalize.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/font-awesome.min.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/icomoon.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/animate.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/prettyPhoto.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/owl.carousel.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/owl.theme.default.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/transitions.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/main.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/color.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/custom.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/css/responsive.css">
        <link rel="stylesheet" href="https://hec.ac.mw/themes/hec/assets/dist/css/app.css">
        
            
        <!-- Global site tag (gtag.js) - Google Analytics -->
        <script async src="https://www.googletagmanager.com/gtag/js?id=G-Y9PMQ0G476"></script>
        <script>
          window.dataLayer = window.dataLayer || [];
          function gtag(){dataLayer.push(arguments);}
          gtag('js', new Date());
        
          gtag('config', 'G-Y9PMQ0G476');
        </script>
    </head>
      <body>
        <!-- Wrapper Start *************************************-->
        <div id="tg-wrapper" class="tg-wrapper">
          <!-- Header -->
          <!--************************************
                Header Start
        *************************************-->
    
    <header id="tg-header" class="tg-header tg-haslayout">
      <div class="tg-topbar">
        <div class="tg-leftbox">
          <span id="tg-datebox" class="tg-datebox"></span>
        </div>
      </div>
      <div class="clearfix"></div>
      <div class="container">
        <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12">
            <div class="tg-logoandnoticeboard">
              <strong class="tg-logo"><a href="/"><img src="https://hec.ac.mw/themes/hec/assets/images/hec-logo-plain.png"
                    alt="Higher Education Central Malawi" width="100" /></a>
              </strong>
              <div class="tg-noticeboard" style="float:left; margin:20px 0 0 10px;">
                <h3 style="font-size:2em; color:#e94d27; font-family:Tahoma; display:inline-block;">
                  Higher Education Central
                </h3>
              </div>
              <div class="tg-noticeboard" style="margin:30px 0 0 10px; border-bottom:1px dotted #ddd;">
                <i class="fa fa-phone" style="color:#e94d27;"></i>&nbsp; 
                <a href="tel:+265 999 808 165"><span>+265 999 808 165</span></a>
                &nbsp;|&nbsp;
                <a href="tel:+265 881 095 672"><span>+265 881 095 672</span></a>
                &nbsp;|&nbsp;
                <i class="fa fa-envelope-o" style="color:#e94d27;"></i>&nbsp;
                <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="cba2a5ada48ba3aea8e5aaa8e5a6bc">[email&#160;protected]</a> &nbsp;|&nbsp;
                <a href="https://www.facebook.com/hecmalawi" target="_blank" title="HEC Facebook"><i class="fa fa-facebook-f fa-lg" style="color:#e94d27;"></i></a>
                &nbsp;&nbsp;|&nbsp;
                <a href="https://www.twitter.com/hecmalawi" target="_blank" title="HEC Twitter"><i class="fa fa-twitter fa-lg" style="color:#e94d27;"></i></a>
                &nbsp;&nbsp;|&nbsp;
                <a href="https://www.linkedin.com/company/hecmalawi" target="_blank" title="HEC LinkedIn"><i class="fa fa-linkedin fa-lg" style="color:#e94d27;"></i></a>
              </div>
            </div>
            <div class="tg-navigationarea">
              <nav id="tg-nav" class="tg-nav">
                <div class="navbar-header">
                  <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#tg-navigation"
                    aria-expanded="false">
                    <span class="sr-only">Toggle navigation</span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                  </button>
                </div>
                <div id="tg-navigation" class="collapse navbar-collapse tg-navigation">
                  <ul>
                    <li class="">
                      <a id="mn_home" href="/">Home</a>
                    </li>
                    <li class="menu-item-has-children ">
                      <a id="mn_students" href="/students/tools" @click="setActiveTab">Students</a>
                      <ul class="sub-menu">
                        <li>
                          <a href="/study/find-college">Find A College</a>
                        </li>
    
                        <li>
                          <a href="/study/find-course">Find a Course</a>
                        </li>
                        <li>
                          <a href="/study/majors">Find College By Major</a>
                        </li>
                        <li>
                          <a href="/scholarships">Scholarships</a>
                        </li>
                        <li>
                          <a href="/study/professional-certifications">Professional Certifications</a>
                        </li>
                        <li>
                          <a href="/study/international-students">For International Students</a>
                        </li>
                       
                      </ul>
                    </li>
                    <li id="mn_institutions" class="menu-item-has-mega-menu "  @click="setActiveTab">
                      <a href="/services">For Institutions</a>
                      <div class="mega-menu">
                        <ul class="mega-menu-row">
                          <li class="mega-menu-col">
                            <ul>
                              <li>
                                <a href="/services">Teaching &amp; Learning Technologies</a>
                              </li>
                              <li>
                                <a href="/services">Media &amp; Marketing</a>
                              </li>
                              <li>
                                <a href="/services">Staff Development (CPD)</a>
                              </li>
                              <li>
                                <a href="/services">Freemium College Listing</a>
                              </li>
                            </ul>
                          </li>
                        </ul>
                        <ul class="mega-menu-row">
                          <li class="mega-menu-col">
                            <div class="tg-textbox" style="display:block;">
                              <strong>HEC Institution Services</strong>
                              <div class="tg-description">
                                <p>
                                  Take the first step in the digital transformation of your institution and get ahead of your competition.
                                </p>
                              </div>
                              <a href="/services" class="tg-btn tg-bgn-sm" href="">learn more!</a>
                            </div>
                          </li>
                        </ul>
                      </div>
                    </li>
                    <li class="menu-item-has-mega-menu ">
                      <a href="/posts">News &amp; Events</a>
                      <div class="mega-menu tg-fullmegamenu">
                        <ul class="mega-menu-row">
                          <li class="mega-menu-col">
                            <div class="tg-themetabs">
                              
                              <div class="tab-content tg-themetabcontent">
                                <div role="tabpanel" class="tab-pane tg-tabpane active" id="tg-science">
                                  <strong>Latest HE News, Announcements &amp; Events</strong>
                                  <div class="tg-posts">
                                    <div id="tg-navtabslider" class="tg-navtabslider tg-megamenuslider owl-carousel">
    
                                      
                                      <!-- LOOP OVER NEWS ITEMS -->
                                                                        <div class="item">
                                        <article class="tg-themepost">
                                          <figure class="tg-featuredimg">
                                            <a href="/post/unima-offer-short-courses-for-secondary-school-science-teachers-and-education-practitioners-2021">
                                                                                        <img src="https://hec.ac.mw/storage/app/uploads/public/04d/27f/456/thumb__194_115_0_0_crop.jpg" title="UNIMA To Offer Short Courses for Secondary School Science Teachers and Education Practitioners">
                                                                                      </a>
                                          </figure>
                                          <div class="tg-themepostcontent">
                                            <span class="menu_tag">
                                              <i class="fa fa-pencil"></i>&nbsp;Short courses
                                            </span>
                                            <div class="tg-themeposttitle">
                                              <h3><a href="/post/unima-offer-short-courses-for-secondary-school-science-teachers-and-education-practitioners-2021">UNIMA To Offer Short Courses for Secondary School Science Teachers and Education Practitioners</a></h3>
                                            </div>
                                            <ul class="tg-matadata">
                                              <li>
                                                <i class="fa fa-clock-o"></i>
                                                <span>
                                                  5 days ago
                                                  &nbsp;|&nbsp;
                                                  <!--<i class="fa fa-eye"></i>&nbsp;2k-->
                                                </span>
                                              </li>
                                            </ul>
    
                                          </div>
                                        </article>
                                      </div>
                                                                        <div class="item">
                                        <article class="tg-themepost">
                                          <figure class="tg-featuredimg">
                                            <a href="/post/call-for-admissions-must-odel-courses-2021-2022">
                                                                                        <img src="https://hec.ac.mw/storage/app/uploads/public/79d/b94/067/thumb__194_115_0_0_crop.jpg" title="Call For Admissions - MUST ODeL Courses for 2021/2022">
                                                                                      </a>
                                          </figure>
                                          <div class="tg-themepostcontent">
                                            <span class="menu_tag">
                                              <i class="fa fa-pencil"></i>&nbsp;Admissions
                                            </span>
                                            <div class="tg-themeposttitle">
                                              <h3><a href="/post/call-for-admissions-must-odel-courses-2021-2022">Call For Admissions - MUST ODeL Courses for 2021/2022</a></h3>
                                            </div>
                                            <ul class="tg-matadata">
                                              <li>
                                                <i class="fa fa-clock-o"></i>
                                                <span>
                                                  2 weeks ago
                                                  &nbsp;|&nbsp;
                                                  <!--<i class="fa fa-eye"></i>&nbsp;2k-->
                                                </span>
                                              </li>
                                            </ul>
    
                                          </div>
                                        </article>
                                      </div>
                                                                        <div class="item">
                                        <article class="tg-themepost">
                                          <figure class="tg-featuredimg">
                                            <a href="/post/malawi-ministry-of-education-releases-selected-names-for-ipte-17-2021">
                                                                                        <img src="https://hec.ac.mw/storage/app/uploads/public/ced/c51/075/thumb__194_115_0_0_crop.jpg" title="MoEST Releases Names of Selected Candidates for IPTE 17">
                                                                                      </a>
                                          </figure>
                                          <div class="tg-themepostcontent">
                                            <span class="menu_tag">
                                              <i class="fa fa-pencil"></i>&nbsp;News
                                            </span>
                                            <div class="tg-themeposttitle">
                                              <h3><a href="/post/malawi-ministry-of-education-releases-selected-names-for-ipte-17-2021">MoEST Releases Names of Selected Candidates for IPTE 17</a></h3>
                                            </div>
                                            <ul class="tg-matadata">
                                              <li>
                                                <i class="fa fa-clock-o"></i>
                                                <span>
                                                  2 weeks ago
                                                  &nbsp;|&nbsp;
                                                  <!--<i class="fa fa-eye"></i>&nbsp;2k-->
                                                </span>
                                              </li>
                                            </ul>
    
                                          </div>
                                        </article>
                                      </div>
                                                                        <div class="item">
                                        <article class="tg-themepost">
                                          <figure class="tg-featuredimg">
                                            <a href="/post/unima-offer-short-courses-in-laboratory-techniques">
                                                                                        <img src="https://hec.ac.mw/storage/app/uploads/public/352/08a/753/thumb__194_115_0_0_crop.jpg" title="UNIMA to Offer Short Courses in Laboratory Techniques">
                                                                                      </a>
                                          </figure>
                                          <div class="tg-themepostcontent">
                                            <span class="menu_tag">
                                              <i class="fa fa-pencil"></i>&nbsp;Short courses
                                            </span>
                                            <div class="tg-themeposttitle">
                                              <h3><a href="/post/unima-offer-short-courses-in-laboratory-techniques">UNIMA to Offer Short Courses in Laboratory Techniques</a></h3>
                                            </div>
                                            <ul class="tg-matadata">
                                              <li>
                                                <i class="fa fa-clock-o"></i>
                                                <span>
                                                  1 month ago
                                                  &nbsp;|&nbsp;
                                                  <!--<i class="fa fa-eye"></i>&nbsp;2k-->
                                                </span>
                                              </li>
                                            </ul>
    
                                          </div>
                                        </article>
                                      </div>
                                      
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </li>
                        </ul>
                      </div>
                    </li>
                    <li class="current-menu-item">
                      <a href="/scholarships">Scholarships</a>
                    </li>
                    <li class="">
                      <a href="/co-curricular-training">Co-curricular</a>
                    </li>
                    <li class=""><a href="/about">About</a></li>
                    <li class=""><a href="/about/contact-us">Contact</a></li>
                  </ul>
                </div>
              </nav>
              <div class="tg-searchbox">
                <a id="tg-btnsearch" class="tg-btnsearch" href=""><i class="icon-magnifier"></i></a>
                <form class="tg-formtheme tg-formsearch">
                  <fieldset>
                    <input type="search" name="search" class="form-control" placeholder="Start Your Search Here" />
                  </fieldset>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </header>
    
    
    <!--- HEADER END -->
          <!-- Content -->
          
    <main id="tg-main" class="tg-main tg-haslayout">
        <div id="app" class="container">
            <div class="row" style="background-color:#eeeeee;">
                <div class="col-xs-12" style="padding:15px 30px; background-color:#f7f7f7">
                  <h3>Scholarship Opportunities</h3>
                  <hr class="brief">            
                  <p class="loud"> HEC Scholarship directory is your window to the latest scholarship and funding opportunities for undergraduate and graduate studies</p>
                  <hr>
                </div>
            </div>
          
            <div class="row">     
             
              
                  <div class="col-xs-12 col-sm-12 col-md-9" style="padding:20px 25px 5px 20px;">
                    
                                        <div class="row">
                                        
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/malawi-wellcome-trust-clinical-research-pre-phd-msc-scholarship"><img src="https://hec.ac.mw/storage/app/uploads/public/616/d1f/5ca/616d1f5cab85f527990300.jpg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/malawi-wellcome-trust-clinical-research-pre-phd-msc-scholarship">Malawi Wellcome Trust Pre-MSC and Pre-PhD Internship Scholarship</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 18 October 2021 by HEC Media
                                    </p>
                                    <p>
                                    Malawi Wellcome Trust Pre-MSC and Pre-PhD Internship Scholarship. Closes 01 November 2021                   
                                    </p>
                                    <a href="/scholarship/malawi-wellcome-trust-clinical-research-pre-phd-msc-scholarship" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/university-of-oslo-norads-norhed-phd-and-msc-scholarships"><img src="https://hec.ac.mw/storage/app/uploads/public/616/68b/5f5/61668b5f5c3c0673129442.jpeg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/university-of-oslo-norads-norhed-phd-and-msc-scholarships">University of Oslo NORAD’s NORHED II  PhD and MSc Scholarships</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 13 October 2021 by HEC Media
                                    </p>
                                    <p>
                                    University of Oslo NORAD’s NORHED II  PhD and MSc Scholarships. Closes 05 November 2021                   
                                    </p>
                                    <a href="/scholarship/university-of-oslo-norads-norhed-phd-and-msc-scholarships" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/nutrition-4-health-activity-scholarship-opportunities-postgraduate-studies-luanar"><img src="https://hec.ac.mw/storage/app/uploads/public/614/ad3/939/614ad39390730888401621.png" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/nutrition-4-health-activity-scholarship-opportunities-postgraduate-studies-luanar">Nutrition 4 Health Activity Scholarship Opportunities For Postgraduate Studies at LUANAR</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 22 September 2021 by HEC Media
                                    </p>
                                    <p>
                                    Nutrition 4 Health Activity Scholarship Opportunities For Postgraduate Studies at LUANAR. Closes 04 October 2021                   
                                    </p>
                                    <a href="/scholarship/nutrition-4-health-activity-scholarship-opportunities-postgraduate-studies-luanar" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                          
                      </div><!-- row -->
    
                                        <div class="row">
                                        
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/global-learning-scholarship-program-glsp"><img src="https://hec.ac.mw/storage/app/uploads/public/614/1e6/76e/6141e676ec7b3283665339.jpg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/global-learning-scholarship-program-glsp">The Global Learning Scholarship Program (GLSP)</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 15 September 2021 by HEC Media
                                    </p>
                                    <p>
                                    The Global Learning Scholarship Program (GLSP). Closes 16 December 2021                   
                                    </p>
                                    <a href="/scholarship/global-learning-scholarship-program-glsp" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/schlumberger-foundation-faculty-for-the-future-fellowships-2022-2023"><img src="https://hec.ac.mw/storage/app/uploads/public/612/622/a9c/612622a9c61b0019281345.png" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/schlumberger-foundation-faculty-for-the-future-fellowships-2022-2023">The Schlumberger Foundation Faculty for the Future Fellowships 2022-2023</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 25 August 2021 by HEC Media
                                    </p>
                                    <p>
                                    The Schlumberger Foundation Faculty for the Future Fellowships 2022-2023. Closes 05 November 2021                   
                                    </p>
                                    <a href="/scholarship/schlumberger-foundation-faculty-for-the-future-fellowships-2022-2023" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/kalinga-institute-industrial-technology-kiit-international-scholarship-program-2021"><img src="https://hec.ac.mw/storage/app/uploads/public/611/37d/458/61137d458ca04405483498.jpg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/kalinga-institute-industrial-technology-kiit-international-scholarship-program-2021">Kalinga Institute of Industrial Technology (KIIT) International Scholarship Program 2021</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 11 August 2021 by HEC Media
                                    </p>
                                    <p>
                                    Kalinga Institute of Industrial Technology (KIIT) International Scholarship Program 2021. Closes 15 August 2021                   
                                    </p>
                                    <a href="/scholarship/kalinga-institute-industrial-technology-kiit-international-scholarship-program-2021" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                          
                      </div><!-- row -->
    
                                        <div class="row">
                                        
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/african-scientific-research-and-innovation-council-asric-scholarship-2021"><img src="https://hec.ac.mw/storage/app/uploads/public/611/253/090/61125309098b2036160708.jpg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/african-scientific-research-and-innovation-council-asric-scholarship-2021">African Scientific, Research and Innovation Council (ASRIC)  Scholarship 2021</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 10 August 2021 by HEC Media
                                    </p>
                                    <p>
                                    African Scientific, Research and Innovation Council (ASRIC)  Scholarship 2021. Closes 31 July 2021                   
                                    </p>
                                    <a href="/scholarship/african-scientific-research-and-innovation-council-asric-scholarship-2021" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/ashinaga-african-initiative-2022"><img src="https://hec.ac.mw/storage/app/uploads/public/611/248/fb8/611248fb86e73762395014.jpg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/ashinaga-african-initiative-2022">The Ashinaga African Initiative 2022</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 10 August 2021 by HEC Media
                                    </p>
                                    <p>
                                    The Ashinaga African Initiative 2022. Closes 28 January 2022                   
                                    </p>
                                    <a href="/scholarship/ashinaga-african-initiative-2022" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                                        
                            <div class="col-xs-12 col-sm-12 col-md-4" style="margin-bottom:25px; padding:0 5px;">                    
                              <div class="post-item">
                                  <div class="scholar-image">
                                    <a href="/scholarship/phd-and-postdoc-positions-in-machine-learning-university-of-amsterdam"><img src="https://hec.ac.mw/storage/app/uploads/public/60e/e55/bb8/60ee55bb8bbca203427422.jpg" class="img-responsive cover"></a>                              </div>
                                          
                                  <div class="scholar-content-box">
                                    <h4 class="scholarship-title">                   
                                      <a href="/scholarship/phd-and-postdoc-positions-in-machine-learning-university-of-amsterdam">PhD and Postdoc Positions in Machine Learning at the University of Amsterdam</a>
                                    </h4>
                                    <p style="margin-bottom:5px;">
                                                      
                                    </p>
                                    <p class="scholar-meta">
                                      <i class="fa fa-pencil"></i>&nbsp;Posted on 14 July 2021 by HEC Media
                                    </p>
                                    <p>
                                    PhD and Postdoc Positions in Machine Learning at the University of Amsterdam. Closes 23 August 2021                   
                                    </p>
                                    <a href="/scholarship/phd-and-postdoc-positions-in-machine-learning-university-of-amsterdam" class="btn btn-warning btn-sm">Read more</a> 
                                  </div>
                              </div>
                            </div>
                          
                      </div><!-- row -->
    
                                    <div class="row pagination">
                      <div class="col-xs-12">
                                          <ul class="pagination">
                                            
                                                        <li class="active">
                                    <a href="https://hec.ac.mw/scholarships/1">1</a>
                                </li>
                                                        <li class="">
                                    <a href="https://hec.ac.mw/scholarships/2">2</a>
                                </li>
                                                        <li class="">
                                    <a href="https://hec.ac.mw/scholarships/3">3</a>
                                </li>
                                                        <li class="">
                                    <a href="https://hec.ac.mw/scholarships/4">4</a>
                                </li>
                                                        <li class="">
                                    <a href="https://hec.ac.mw/scholarships/5">5</a>
                                </li>
                                                        <li class="">
                                    <a href="https://hec.ac.mw/scholarships/6">6</a>
                                </li>
                                                        <li class="">
                                    <a href="https://hec.ac.mw/scholarships/7">7</a>
                                </li>
                                            
                                                        <li><a href="https://hec.ac.mw/scholarships/2">Next &rarr;</a></li>
                                                </ul>
                                      </div>
                  </div>
              </div><!-- results -->
    
              <div class="col-xs-12 col-sm-12 col-md-3" style="padding-top:15px;">
                
                <div class="tg-widget top-list">
                  <div class="tg-borderheading">
                      <h2 class="scream">Other Links</h2>
                  </div>
                  <div>                
                      <ul class="record-list">                   
                          <li> <a href="/study/find-college">College Listing A-Z</a> </li>
                          <li> <a href="/study/majors">Find College By Major</a> </li>
                          <li> <a href="/study/find-course">Find Courses</a> </li>
                          <li> <a href="/study/professional-certifications">Professional Certifications</a> </li>
                          <li> <a href="/students/tools">Student Tools</a></li>
                          <li> <a href="/co-curricular-training">Co-curricular Training</a> </li>
                      </ul>
                  </div>
                </div>
    
              </div>
    
             
            
    
        </div>
    </main>
          <!-- Footer -->
          <!--************************************
    				Footer Start
    		*************************************-->
    <footer id="tg-footer" class="tg-footer tg-haslayout">
        <div class="signup-box">
            <div class="container">
               
                <div class="tg-signuptextbox">
                    <h3><i class="fa fa-newspaper-o"></i>&nbsp;Free Newsletter Signup!</h3>
                    <hr class="brief">
                    <div class="tg-description"><p style="color:#333; font-size:1.1em;">Subscribe to the HEC Newsletter and receive instant updates in your inbox.</p></div>
                </div>
            
                <div class="tg-description" style="margin-top:15px;">
                    <button type="button" class="btn btn-warning btn-md" data-toggle="modal" data-target="#subscribeModal">Subscribe</button>
                </div>
                
            </div>
        </div>
        <div class="tg-footermiddlebar">
            <div class="container">
                <div class="row">
                    <div class="col-xs-12 col-sm-6 col-md-3 col-lg-3">
                        <div class="tg-widget tg-widgetcompanyinfo">
                            <div class="tg-widgetcontent">
                                <strong class="tg-logo"><a href="/"><img src="https://hec.ac.mw/themes/hec/assets/images/hec-logo-plain.png" width="150" alt="Higher Education Central Malawi"></a></strong>
                                <div class="tg-description">
                                    <p>The most trusted source of higher education resources and services.
                                    <br><br>
                                    <a href="/about">Read more..</a></p>
                                </div>
                                <ul class="tg-infolist">
                                    <li>
                                        <i class="icon-phone-handset"></i>
                                        <a href="tel:+265 999 808 165"><span>+265 999 808 165</span></a>
                                    </li>
                                    <li>
                                        <i class="icon-phone-handset"></i>
                                        <a href="tel:+265 881 095 672"><span>+265 881 095 672</span></a>
                                    </li>
                                    <li>
                                        <a href="/cdn-cgi/l/email-protection#2e474048416e464b4d004f4d004359">
                                            <i class="icon-envelope"></i>
                                            <span><span class="__cf_email__" data-cfemail="85ecebe3eac5ede0e6abe4e6abe8f2">[email&#160;protected]</span></span>
                                        </a>
                                    </li>
                                </ul>
                                
                            </div>
                        </div>
                    </div>
                    <div class="col-xs-12 col-sm-6 col-md-2 col-lg-2">
                        <div class="tg-widget tg-widgetcoursecategories">
                            <div class="tg-widgettitle">
                                <h3>For Students</h3>
                            </div>
                           
                                <ul class="footer_list">
                                    <li><a href="/study/find-college">College Listing A-Z</a></li>
                                    <li><a href="/study/find-course">Find a Course</a></li>
                                    <li><a href="/scholarships">Funding &amp; Scholarships</a></li>
                                    <li><a href="/students/admission-tools">Student Tools</a></li>
                                    <li><a href="/co-curricular-training">Co-curricular Training</a></li>
                                    <li><a href="http://www.hec.academy">HEC Academy</a></li>
                                    <li><a href="/study/international-students">International Students</a></li>
                                    <li><a href="/study/majors">Browse Majors</a></li>
                                </ul>
                                                       
                        </div>
                    </div>
                    <div class="col-xs-12 col-sm-6 col-md-3 col-lg-3">
                        <div class="tg-widget tg-widgetcoursecategories">
                            <div class="tg-widgettitle">
                                <h3>For Institutions</h3>
                            </div>                       
                                <ul class="footer_list">
                                    <li><a href="/services">Media &amp; Marketing</a></li>
                                    <li><a href="/services">Continuous Professional Development</a></li>
                                    <li><a href="/services">Free Course &amp; College Listing</a></li>
                                    <li><a href="/services">Learning &amp; Teaching Technologies</a></li>                                
                                </ul>      
                            </div>
                         </div>
                    <div class="col-xs-12 col-sm-6 col-md-4 col-lg-4">
                        <div class="tg-widget tg-widgetflickrgallery">
                            <div class="tg-widgettitle">
                                <h3>Relevant Links</h3>
                            </div>
                            <ul class="footer_list">
                                <li><a href="http://www.nche.ac.mw" target="_blank">National Council for Higher Education (NCHE)</a></li>
                                <li><a href="https://www.heslgb.mw" target="_blank">HE Loans &amp; Grants Board (HESLGB)</a></li>
                                <li><a href="https://www.ncst.mw" target="_blank">The National Commission For Science &amp; Technology (NCST)</a></li>
                                <li><a href="https://www.teveta.mw" target="_blank">TEVET Authority</a></li>
                                <li><a href="https://www.education.gov.mw" target="_blank">Ministry of Education, Science &amp; Technology</a></li>
                                <li><a href="https://ucamalawi.com" target="_blank">Universities and Colleges Association of Malawi (UCAM)</a></li>                          
                            </ul>
                            <hr>
                           
                            <div style="margin:5px 0 0 10px; font-size:1.3em; text-align:left;">
                                <div class="tg-widgettitle">
                                    <h3 style="font-size:0.8em;">Follow HEC on social media</h3>
                                </div>
                                <a href="https://www.facebook.com/hecmalawi" target="_blank" title="HEC Facebook Page"><i class="fa fa-facebook-f fa-lg" style="color:#e94d27;"></i></a>
                                &nbsp;&nbsp;|&nbsp;
                                <a href="https://www.twitter.com/hecmalawi" target="_blank" title="HEC Twitter Page"><i class="fa fa-twitter fa-lg" style="color:#e94d27;"></i></a>
                                &nbsp;&nbsp;|&nbsp;
                                <a href="https://www.linkedin.com/company/hecmalawi" target="_blank" title="HEC LinkedIn Page"><i class="fa fa-linkedin fa-lg" style="color:#e94d27;"></i></a>
                            </div>
                            
                        </div>
                    </div>
                </div>
            </div>
    
        
            <!-- Modal -->
            <div id="subscribeModal" class="modal fade" role="dialog">
                <div class="modal-dialog">
                    <!-- Modal content-->
                    <div class="modal-content">
                        <div class="modal-header" style="border-bottom:0;">
                            <button type="button" class="close" data-dismiss="modal">&times;</button>                      
                        </div>
                       
                        <div class="modal-body" style="text-align:center; padding:20px 50px 40px 50px;">
                            <h3 style="color:orangered; font-weight:600; padding-bottom:15px; border-bottom:1px solid #ddd;">
                               <i class="fa fa-newspaper-o"></i>&nbsp; JOIN OUR NEWSLETTER!
                            </h3>
    
                            <h5>Be the First To Know!</h5>
    
                            <p>Subscribe and receive the latest college news, announcements, events and scholarship updates!</p>
                            <div class="magic-form">
                                 <form data-request="onSendSubscription" data-request-redirect="https://hec.ac.mw/scholarships">
    
        <input name="_token" type="hidden" value="AcItc8Qi0x8WL5hlIRvtQs2L1TXRDnGHXIBHSkQG">
    
        <div class="form-group span-right">
            <label>Name:</label>
            <input type="text" name="name" value="" class="form-control" required>
        </div>
    
        <div class="form-group span-right">
            <label>Email address:</label>
            <input type="email" name="email" value="" class="form-control" required>
        </div>
        
        <div class="form-group span-right">
            <div data-validate-for="subject"></div>
            <label>Where Do You Fit?</label>
            <select id="profile" name="profile" class="form-control" required>
                <option value="general">-- Would rather not say --</option>
                <option value="secondary">Still in secondary/high school</option>
                <option value="gapyear">In my gap year</option>
                <option value="undergraduate">Undergraduate student</option>
                <option value="postgraduate">Postgraduate student</option>
                <option value="international">International student</option>
                <option value="academic">Academic or researcher</option>
            </select> 
        </div>
        
        <button id="subscriptionSubmitButton" type="submit" class="btn btn-warning btn-lg btn-block">Subscribe</button>
    
    </form>                        </div>                
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="tg-footerbar">
            <div class="container">
                <div class="row">
                    <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12">
                        <span class="tg-copyright">&copy; 2021 Copyright HEC. All Rights Reserved</span>
                        &nbsp;|&nbsp;                    
                        <span>Developed and maintained by <a href="/services" style="color:#ccc; font-decoration:underline;">HEC Media</a></span>
                        <nav class="tg-addnav">
                            <ul>
                                <li><a href="/about/privacy-policy">Privacy Policy</a></li>
                                <li><a href="/about/terms-and-conditions">Terms &amp; Conditions</a></li>
                                <li><a href="/about/contact-us">Contact us</a></li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
        </div>
    </footer>
    <!--************************************
            Footer End
    *************************************-->
    </div>
    <!--************************************
            Wrapper End
    *************************************-->    </div>
        <!-- Wrapper end -->
    
        <!-- Scripts -->
        <script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script src="https://hec.ac.mw/themes/hec/assets/js/vendor/modernizr-2.8.3-respond-1.4.2.min.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/vendor/jquery-library.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/vendor/bootstrap.min.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/owl.carousel.min.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/isotope.pkgd.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/prettyPhoto.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/collapse.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/moment.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/main.js"></script>
    <script src="https://hec.ac.mw/themes/hec/assets/js/vue/vue.js"></script>
        <script src="/modules/system/assets/js/framework.combined-min.js"></script>
    <link rel="stylesheet" property="stylesheet" href="/modules/system/assets/css/framework.extras-min.css">
    
         <!-- Injected scripts -->
         
        
      </body>
    </html>
    


```python
soup = BeautifulSoup(res.text, 'html5lib')
#print(soup.prettify())
```


```python
#g_text = soup.find('div', class_ = 'scholar-content-box')
#print(BeautifulSoup(g_text.text, 'html5lib'))
```


```python
#Empty list sequences for later usage => capturing data for the 3 columns
scholarship_names = []
creation_dates = []
closing_dates = []


#Extract the entire parent block housing the single scholarship details,i.e. html tags included
main_content_extract = soup.find_all('div', class_ = 'scholar-content-box')


#Get the total number of scholarships. Crucial for looping below
list_length = len(main_content_extract)

#Loop through the main_content_exctract
for i in range(int(list_length)):
    #Append the scholarship name by index
    scholarship_names.append(main_content_extract[i].h4.a.text)
               
    #Capture the full text with the posted on string included
    full_str_post_date = main_content_extract[i].find_all('p')[1].text
     
    #Extract only the date .format = {day month year}    
    full_str_close_date = main_content_extract[i].find_all('p')[-1].text
    
    #recombination of the extracted values into a string
    creation_date_extract =  " ".join(full_str_post_date.split(" ")[36:39])
               
    #Append the creation date by index after prep
    creation_dates.append(creation_date_extract)
    
    #Capture the closing date 
    split_closing_date = full_str_close_date.split(".")
               
    closing_date_extract = " ".join(split_closing_date[-1].split(" ")[2:-1])
            
    #print(closing_date_extract)
                
    #Append the closing date
    closing_dates.append(closing_date_extract)

#print(scholarship_names)
#print(creation_dates)
#print(closing_dates)
#
#print(closing_date_extract)
```


```python
import pandas as pd 

scholarship_details = pd.DataFrame({'date_posted': creation_dates, 'scholarchip_name': scholarship_names, 'deadline':closing_dates})
```


```python
scholarship_details.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>date_posted</th>
      <th>scholarchip_name</th>
      <th>deadline</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>18 October 2021</td>
      <td>Malawi Wellcome Trust Pre-MSC and Pre-PhD Inte...</td>
      <td>01 November 2021                   \n         ...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>13 October 2021</td>
      <td>University of Oslo NORAD’s NORHED II  PhD and ...</td>
      <td>05 November 2021                   \n         ...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>22 September 2021</td>
      <td>Nutrition 4 Health Activity Scholarship Opport...</td>
      <td>04 October 2021                   \n          ...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>15 September 2021</td>
      <td>The Global Learning Scholarship Program (GLSP)</td>
      <td>16 December 2021                   \n         ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>25 August 2021</td>
      <td>The Schlumberger Foundation Faculty for the Fu...</td>
      <td>05 November 2021                   \n         ...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>11 August 2021</td>
      <td>Kalinga Institute of Industrial Technology (KI...</td>
      <td>15 August 2021                   \n           ...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>10 August 2021</td>
      <td>African Scientific, Research and Innovation Co...</td>
      <td>31 July 2021                   \n             ...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>10 August 2021</td>
      <td>The Ashinaga African Initiative 2022</td>
      <td>28 January 2022                   \n          ...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>14 July 2021</td>
      <td>PhD and Postdoc Positions in Machine Learning ...</td>
      <td>23 August 2021                   \n           ...</td>
    </tr>
  </tbody>
</table>
</div>


