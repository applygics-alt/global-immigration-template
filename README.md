<?xml version="1.0" encoding="UTF-8" ?>
<b:template xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b'>
  <b:skin><![CDATA[
    /* ---------- General Styles ---------- */
    body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f5f5f5; color:#333; }
    a { color:#007BFF; text-decoration:none; }
    a:hover { text-decoration:underline; }

    /* ---------- Header ---------- */
    #header {
      background:#004080;
      color:#fff;
      padding:15px 20px;
      position:sticky;
      top:0;
      z-index:999;
      display:flex;
      align-items:center;
      justify-content:space-between;
      flex-wrap:wrap;
    }
    #header img { height:50px; }
    #header nav a { margin-left:20px; color:#fff; font-weight:bold; }

    /* ---------- Hero Slider ---------- */
    #hero {
      width:100%;
      height:400px;
      background:url('https://www.globalimmigration.in/hero-banner.jpg') center/cover no-repeat;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      color:#fff;
      position:relative;
    }
    #hero h1 { font-size:2.5em; background:rgba(0,0,0,0.5); padding:10px 20px; border-radius:10px; }
    #hero a.cta { margin-top:15px; display:inline-block; background:#ff9900; color:#fff; padding:10px 20px; border-radius:5px; font-weight:bold; text-decoration:none; }

    /* ---------- Main Wrapper ---------- */
    #main-wrapper { display:flex; max-width:1200px; margin:20px auto; gap:20px; }

    #content { flex:3; display:grid; grid-template-columns:1fr; gap:20px; }
    .post { background:#fff; padding:20px; box-shadow:0 0 15px rgba(0,0,0,0.1); border-radius:10px; }
    .post h2 { color:#004080; margin-bottom:10px; }
    .post p { line-height:1.6; }

    /* ---------- Featured Services ---------- */
    #services { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; margin:40px 0; }
    .service-card { background:#fff; padding:20px; border-radius:10px; text-align:center; box-shadow:0 0 15px rgba(0,0,0,0.1); }
    .service-card h3 { color:#004080; margin-bottom:10px; }
    .service-card p { line-height:1.4; }

    /* ---------- Sidebar ---------- */
    #sidebar { flex:1; background:#fff; padding:20px; box-shadow:0 0 10px rgba(0,0,0,0.1); border-radius:10px; }
    #sidebar h3 { color:#004080; margin-bottom:10px; }
    #sidebar ul { list-style:none; padding:0; }
    #sidebar ul li { margin-bottom:10px; }

    /* ---------- Footer ---------- */
    #footer { background:#004080; color:#fff; text-align:center; padding:15px 20px; margin-top:20px; }

    /* ---------- Responsive ---------- */
    @media (max-width:768px){
      #main-wrapper { flex-direction:column; }
      #header { flex-direction:column; align-items:flex-start; }
      #header nav { margin-top:10px; }
      #hero { height:250px; }
    }
  ]]></b:skin>

  <!-- ---------- Header ---------- -->
  <b:section id="header-section" class="header-section" maxwidgets="1" showaddelement="no">
    <b:widget id="Header1" type="Header" version="2" locked="true" title="">
      <b:widget-settings>
        <b:widget-setting name="displayName">Global Immigration Consultant</b:widget-setting>
        <b:widget-setting name="image">https://www.globalimmigration.in/logo.png</b:widget-setting>
      </b:widget-settings>
      <b:includable id="main">
        <div id="header">
          <img expr:src='data:blog.pageTitle &amp; "/logo.png"' alt="Global Immigration Consultant"/>
          <nav>
            <a expr:href='data:blog.homepageUrl'>Home</a>
            <a href="#services">Services</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
          </nav>
        </div>
      </b:includable>
    </b:widget>
  </b:section>

  <!-- ---------- Hero Section ---------- -->
  <div id="hero">
    <div>
      <h1>Your Trusted Immigration Partner Worldwide</h1>
      <a class="cta" href="#contact">Get Consultation</a>
    </div>
  </div>

  <!-- ---------- Main Wrapper ---------- -->
  <div id="main-wrapper">
    <!-- Content -->
    <div id="content">
      <!-- Featured Services -->
      <div id="services">
        <div class="service-card">
          <h3>USA Work Visa</h3>
          <p>Expert guidance for employment-based visas to the USA.</p>
        </div>
        <div class="service-card">
          <h3>Canada Business Visa</h3>
          <p>Professional consultancy for Canadian business immigration.</p>
        </div>
        <div class="service-card">
          <h3>Student Visa</h3>
          <p>Complete support for studying abroad in top universities.</p>
        </div>
        <div class="service-card">
          <h3>Family Sponsorship</h3>
          <p>Help with family reunification visas globally.</p>
        </div>
      </div>

      <!-- Blog Posts -->
      <b:section id="main" class="main-section" maxwidgets="1" showaddelement="no">
        <b:widget id="Blog1" type="Blog" version="2" locked="true" title="">
          <b:includable id="main">
            <b:loop values='data:posts' var='post'>
              <div class="post">
                <h2><data:post.title/></h2>
                <p><data:post.body/></p>
              </div>
            </b:loop>
          </b:includable>
        </b:widget>
      </b:section>
    </div>

    <!-- Sidebar -->
    <div id="sidebar">
      <b:section id="sidebar1" class="sidebar" maxwidgets="5" showaddelement="yes">
        <b:widget id="HTML1" type="HTML" version="2" locked="false" title="About Us">
          <b:widget-settings>
            <b:widget-setting name="content">
              <p>Global Immigration Consultant is your trusted partner for immigration services worldwide. Expert guidance for visas, employment, and business immigration.</p>
            </b:widget-setting>
          </b:widget-settings>
        </b:widget>

        <b:widget id="PopularPosts1" type="PopularPosts" version="2" title="Popular Posts">
          <b:widget-settings>
            <b:widget-setting name="numPosts">5</b:widget-setting>
          </b:widget-settings>
        </b:widget>
      </b:section>
    </div>
  </div>

  <!-- Footer -->
  <b:section id="footer-section" class="footer-section" maxwidgets="1" showaddelement="no">
    <b:widget id="Footer1" type="HTML" version="2" locked="true" title="">
      <b:includable id="main">
        <div id="footer">
          &copy; 2026 Global Immigration Consultant. All rights reserved.
        </div>
      </b:includable>
    </b:widget>
  </b:section>
</b:template>