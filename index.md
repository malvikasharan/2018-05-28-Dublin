---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "dc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "Computational Skills for Data Analysis (Data Carpentry)"        # brief name of host site without address (e.g., "Euphoric State University")

address: "B003, UCD School of Computer Science, UCD, Belfield"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "ie"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1)
language: "En"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/ISO_639-1)
latlng: "53.142367, -7.692054"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use http://www.latlong.net/)
humandate: "May 28-29, 2018"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 am - 5:00 pm"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2018-05-28      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2018-05-28        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Jason Williams, Malvika Sharan, Bérénice Batut"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Norman Davey (Host), Danielle Quinn, Jean Manguy, Chiara Cotroneo, Benjamin Roques, TBA"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["malvika.sharan@embl.de, norman.davey@ucd.ie"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: http://pad.software-carpentry.org/2018-05-28-Dublin            # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite: 
# optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
  HEADER

  Edit the values in the block above to be appropriate for your workshop.
  If the value is not 'true', 'false', 'null', or a number, please use
  double quotation marks around the value, unless specified otherwise.
  And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

{% comment %}
  EVENTBRITE

  This block includes the Eventbrite registration widget if
  'eventbrite' has been set in the header.  You can delete it if you
  are not using Eventbrite, or leave it in, since it will not be
  displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="248px"
  scrolling="auto">
</iframe>
{% endif %}

<h2 id="general">General Information</h2>

{% comment %}
  INTRODUCTION

  Edit the general explanatory paragraph below if you want to change
  the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
  {% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/intro.html %}
{% endif %}

{% comment %}
  AUDIENCE

  Explain who your audience is.  (In particular, tell readers if the
  workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
  {% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/who.html %}
{% endif %}

{% comment %}
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the workshop have been set.  You
  can use http://itouchmap.com/latlong.html to find the lat/long of an
  address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="https://www.openstreetmap.org/way/23653391#map=17/53.30878/-6.22165">OpenStreetMap</a>
  or
  <a href="https://www.google.ie/maps/place/UCD+School+of+Computer+Science/@53.3092609,-6.2260722,17z/data=!3m1!4b1!4m5!3m4!1s0x486709309a5b7149:0x80dd297b516d89b5!8m2!3d53.3092609!4d-6.2238835?shorturl=1">Google Maps</a>.
</p>
{% endif %}

{% comment %}
  DATE

  This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges
  on. They should have a few specific software packages installed (listed
  <a href="#setup">below</a>). They are also required to abide by
  {% if page.carpentry == "swc" %}
  Software Carpentry's
  {% elsif page.carpentry == "dc" %}
  Data Carpentry's
  {% elsif page.carpentry == "lc" %}
  Library Carpentry's
  {% endif %}
  <a href="{{site.swc_site}}/conduct.html">Code of Conduct</a>.
</p>

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Course materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you please get in touch (using contact details below) and we will
  attempt to provide them.
</p>

<p id="Registration">
  <strong>Registration:</strong> 
  Please note that the course is primarily open for the academic researchers from UCD and UCD affiliated institutes. If you are from other research institute and would like to attend the course, please contact the organizers personally.
</p>

<p>
 <a href="https://www.hd-hub.de/course-dates/3-all/28-data-carpentry-dublin">REGISTER HERE</a>
</p>

<p>Each registration will be reviewed and applicants will be confirmed for their participation via email by the organisers.</p>

{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

{% comment %}
  SCHEDULE

  Show the workshop's schedule.  Edit the items and times in the table
  to match your plans.  You may also want to change 'Day 1' and 'Day
  2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

{% comment %} DO NOT EDIT SURVEY LINKS {% endcomment %}
<p><em>Surveys</em></p>
{% if page.carpentry == "swc" %} 
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.swc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.swc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif page.carpentry == "dc" %}
  <p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.dc_pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.dc_post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% elsif page.carpentry == "lc" %}
<p>Ask your instructor about pre- and post-workshop Survey details.</p>
{% endif %}


{% if page.carpentry == "swc" %}
  {% include sc/schedule.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/schedule.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/schedule.html %}
{% endif %}

{% comment %}
  Collaborative Notes

  If you want to use an Etherpad, go to

      http://pad.software-carpentry.org/YYYY-MM-DD-site

  where 'YYYY-MM-DD-site' is the identifier for your workshop,
  e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

{% comment %}
  SYLLABUS

  Show what topics will be covered.

  1. If your workshop is R rather than Python, remove the comment
     around that section and put a comment around the Python section.
  2. Some workshops will delete SQL.
  3. Please make sure the list of topics is synchronized with what you
     intend to teach.
  4. You may need to move the div's with class="col-md-6" around inside
     the div's with class="row" to balance the multi-column layout.

  This is one of the places where people frequently make mistakes, so
  please preview your site before committing, and make sure to run
  'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>

{% if page.carpentry == "swc" %}
  {% include sc/syllabus.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/syllabus.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/syllabus.html %}
{% endif %}

<hr/>

{% comment %}
  SETUP

  Delete irrelevant sections from the setup instructions.  Each
  section is inside a 'div' without any classes to make the beginning
  and end easier to find.

  This is the other place where people frequently make mistakes, so
  please preview your site before committing, and make sure to run
  'tools/check' as well.
{% endcomment %}
<br>
<p></p>
<h2 id="setup">Setup</h2>
<p>
  To participate in a Data Carpentry workshop,
  you will need working copies of the software described below.
  Please make sure to install everything and try opening it to make sure it works
  <em>before</em> the start of your workshop. If you run into any problems,
please feel free to email the instructor or arrive early to your workshop on
the first day.
Participants should bring and use their own laptops to insure the proper setup of
tools for an efficient workflow once you leave the workshop.
</p>

<h3 id="platform_specfic">Platform-specific Notes</h3>
<p>This workshop will be using the software outlined in the install instructions below.
Please see the section for your operating system for those directions.
</p><ul>
<li><a href="#windows">Windows</a>
</li><li><a href="#mac">Mac</a>
</li><li><a href="#linux">Linux</a>
</li></ul>

<h3 id="windows">Windows</h3>
<p>
Please go through all the installation steps below and make sure that
you not only installed them, but start them up to make sure they're working.
If you have any problems, don't hesitate to email the instructors to
ask for help, or arrive early on the first day of the workshop to
get help.
</p>
<div class="row-fluid">
<ol>
<li><b>A spreadsheet program</b></li>
<br>For this workshop you will need a spreadsheet program. Many people already have
Microsoft Excel installed, and if you do, you're set!
<br>
If you need a spreadsheet
program, there are a few other options, like OpenOffice and LibreOffice. Install
instructions for LibreOffice, which is free and open source, are here.
       <ul>
          <li><b>Download the Installer</b>
        <br>Install LibreOffice by going to the <a href="https://www.libreoffice.org/download/libreoffice-fresh/">installation page</a>. The version for Windows
should automatically be selected. Click <b>Download Version 6.0.3 or later</b>. You
will go to a page that asks about a donation, but you don't need to make one.
Your download should begin automatically.
          </li><li><b>Install LibreOffice</b>
            <br>Once the installer is downloaded, double click on it and it should install.
</li><li>To use LibreOffice, double click on the icon and it will open.
</li></ul>
<li><b>Putty</b></li>
<br>You will need a terminal program to access the AWS Cloud/HPC cluster.
<ul>
<li>Go to the Putty <a href="http://www.chiark.greenend.org.uk/%7Esgtatham/putty/download.html">download
page</a>
</li><li>Click on <i>putty.exe</i> link to download the install file
</li><li>To use it, double-click on the downloaded file
</li><li>Follow any installation instructions, if any
</li></ul>
<li><b>FTP Client (Filezilla)</b></li>
<br>An FTP client will help you transfer files easily between your computer and the cloud.
<ul>
<li>Go to the Filezila <a href="https://filezilla-project.org/download.php?show_all=1">download
page</a>
</li><li>Chose the download link appropriate to your system
</li><li>To use it, double-click on the downloaded file
</li><li>Follow any installation instructions, if any
</li><li>At the workshop we will give you additional information (e.g. host, username, port) to connect
</li></ul>
<li><b>R</b></li>
<br>In the workshop, we will use RStudio. RStudio is a nice interface to the
programming language R. To use RStudio, you need to install both R and RStudio.
<ul>
<li>      Download R from
      <a href="http://cran.r-project.org/bin/windows/base/release.htm">here</a>
</li><li>Run the .exe file that was just downloaded
</li><li>Go to the <a href="http://www.rstudio.com/ide/download/desktop">RStudio Download page</a>
</li><li>Under <i>Installers</i> select <b>RStudio 1.1.447 or later - Windows XP/Vista/7/8</b>
</li><li>Double click the file to install it
</li><li>Once it's installed, open RStudio to make sure it works and you don't get any error messages.
</li></ul>
<li><b>IGV</b>
<br>If time permits, we will use The Broad Institute's IGV (Integrated Genome Viewer) for
looking at SAM and BAM files, SNPs, and variant calls.
<ul>
<li>To download IGV, please visit
<a href="https://www.broadinstitute.org/software/igv/log-in">this page</a>
 and log in. Please register if you do not already have a login.</li>
<li>Click on the large button for the Download Binary Distribution</li>
<li>Find the zip archive on your computer and expand it</li>
<li>To run IGV, double-click on the IGV.bat file.</li>
</ul>
</li></ol></div>

<h3 id="mac">Mac</h3>
<p>
Please go through all the installation steps below and make sure that
you not only installed them, but start them up to make sure they're working.
If you have any problems, don't hesitate to email the instructors to
ask for help, or arrive early on the first day of the workshop to
get help.
</p><div class="row-fluid">
<ol>
<li><b>A spreadsheet program</b>
<br>For this workshop you will need a spreadsheet program. Many people already have
Microsoft Excel installed, and if you do, you're set!
<br>
If you need a spreadsheet
program, there are a few other options, like OpenOffice and LibreOffice. Install
instructions for LibreOffice, which is free and open source, are here.
       <ul>
          <li><b>Download the Installer</b>
        <br>Install LibreOffice by going to the <a href="https://www.libreoffice.org/download/libreoffice-fresh/">installation page</a>. The version for Mac
should automatically be selected. Click <b>Download Version 6.0.3 or later</b>. You
will go to a page that asks about a donation, but you don't need to make one.
Your download should begin automatically.
          </li><li><b>Install LibreOffice</b>
            <br>Once the installer is downloaded, double click on it and it should install.
</li><li>To use LibreOffice, double click on the icon and it will open.
</li></ul>

<p>
</p></li><li><b>FTP Client (Filezilla)</b>
<br>An FTP client will help you transfer files easily between your computer and the cloud.
<ul>
<li>Go to the Filezila <a href="https://filezilla-project.org/download.php?show_all=1">download
page</a>
</li><li>Chose the download link appropriate to your system
</li><li>To use it, double-click on the downloaded file
</li><li>Follow any installation instructions, if any
</li><li>At the workshop we will give you additional information (e.g. host, username, port) to connect
</li></ul>
</li>
<p><li><b>R</b>
<br>In the workshop, we will use RStudio. RStudio is a nice interface to the
programming language R. To use RStudio, you need to install both R and RStudio.
<ul>
<li>Go to <a href="http://cran.r-project.org/">CRAN</a> and click on <i>Download
R for (Mac) OS X</i>
</li><li>Select the .pkg file for the version of OS X that you have and the file
will download.
</li><li>Double click on the file that was downloaded and R will install
</li><li>Go to the <a href="http://www.rstudio.com/ide/download/desktop">RStudio Download page</a>
</li><li>Under <i>Installers</i> select <b>RStudio 1.1.447 or later - Mac OS X 10.6+ (64-bit)</b> to download it.
</li><li>Once it's downloaded, double click the file to install it
</li><li>Once it's installed, open RStudio to make sure it works and you don't get any error messages.
</li></ul>
<p><li><b>IGV</b></li>
<br>If time permits, we will use The Broad Institute's IGV (Integrated Genome Viewer) for
	looking at SAM and BAM files, SNPs, and variant calls.</p>
<ul>
<li>To download IGV, please visit
<a href="https://www.broadinstitute.org/software/igv/log-in">this page</a>
 and log in. Please register if you do not already have a login.</li>
<li>Click on the large button for the Download Binary Distribution</li>
<li>Find the zip archive on your computer and expand it</li>
<li>To run IGV, double-click on the IGV.bat file.</li>
</ul>

</li></p></ol>
<h3 id="linux">Linux</h3>
<p>
Please go through all the installation steps below and make sure that
you not only installed them, but start them up to make sure they're working.
If you have any problems, don't hesitate to email the instructors to
ask for help, or arrive early on the first day of the workshop to
get help.
</p><div class="row-fluid">
<ol>
<li><b>A spreadsheet program</b>
<br>For this workshop you will need a spreadsheet program. Many people already have
Microsoft Excel installed, and if you do, you're set!
<br>
If you need a spreadsheet
program, there are a few other options, like OpenOffice and LibreOffice. Install
instructions for LibreOffice, which is free and open source, are here.
       <ul>
          <li><b>Download the Installer</b>
        <br>Install LibreOffice by going to the <a href="https://www.libreoffice.org/download/libreoffice-fresh/">installation page</a>. The version for Linux
should automatically be selected. Click <b>Download Version 6.0.3 or later</b>. You
will go to a page that asks about a donation, but you don't need to make one.
Your download should begin automatically.
          </li><li><b>Install LibreOffice</b>
            <br>Once the installer is downloaded, double click on it and it should install.
</li><li>To use LibreOffice, double click on the icon and it will open.
</li></ul>
</li><li><b>FTP Client (Filezilla)</b>
<br>An FTP client will help you transfer files easily between your computer and the cloud.
<ul>
<li>Go to the Filezila <a href="https://filezilla-project.org/download.php?show_all=1">download
page</a>
</li><li>Chose the download link appropriate to your system
</li><li>To use it, double-click on the downloaded file
</li><li>Follow any installation instructions, if any
</li><li>At the workshop we will give you additional information (e.g. host, username, port) to connect
</li></ul>



<p><li><b>R</b>
<br>In the workshop, we will use RStudio. RStudio is a nice interface to the
programming language R. To use RStudio, you need to install both R and RStudio.
<ul>
<li>R is available through most Linux package managers.
You can download the binary files for your distribution
        from <a href="http://cran.r-project.org/index.html">CRAN</a>. Or
        you can use your package manager (e.g. for Debian/Ubuntu
        run <code>sudo apt-get install r-base</code> and for Fedora run
        <code>sudo yum install R</code>).
</li><li>To install RStudi, go to the <a href="http://www.rstudio.com/ide/download/desktop">RStudio Download page</a>
</li><li>Under <i>Installers</i> select the version for your distribution.
</li><li>Once it's downloaded, double click the file to install it
</li><li>Once it's installed, open RStudio to make sure it works and you don't get any error messages.
</li></ul>
<p>
</p></li>
<p><li><b>IGV</b>
<br>If time permits, we will use The Broad Institute's IGV (Integrated Genome Viewer) for
looking at SAM and BAM files, SNPs, and variant calls.
<ul>
<li>To download IGV, please visit
<a href="https://www.broadinstitute.org/software/igv/log-in">this page</a>
 and log in. Please register if you do not already have a login.
<li>Click on the large button for the Download Binary Distribution
<li>Find the zip archive on your computer and expand it
<li>To run IGV, double-click on the IGV.bat file.


<h2 id="syllabus">Course Affiliations</h2>
<p><img src="http://www.ipposi.ie/wp-content/uploads/2017/03/UCD-logo.png" width="80" height="80" /> 
<img src="https://carpentries.org/assets/img/TheCarpentries.svg" width="206" height="42" /> 
&nbsp; &nbsp;<img src="https://tess.elixir-europe.org/system/content_providers/images/000/000/063/original/deNBI_Logo_rgb.jpg?1480590048" width="187" height="49" />
<img src="http://www.publichealth.cam.ac.uk/funding/wp-content/uploads/2017/01/Wellcome_Trust_logo.svg_.png" width="90" height="90"/>
</p>
<p></p>
