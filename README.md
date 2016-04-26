# dx-portfolio 0.8.3
## Content Update Notes
---
### Particle JS Config File
Simply replace `/js/particlesjs-config.json`
### CSS Files
Color Accent: `/less/royal-purple.less` 
Common Colors/Styles: `/less/variables.less`

**NOTE: highly suggest generate CSS with LESS compiler, instruction in Dev Notes towards bottom**

### HTML
#### Navigation
The `href` values here match to the ID of the portfolio sections below wrapped in `<section>` tags
```
<nav class="col-xs-12 col-lg-2 col-lg-offset-8">
	<ul id="side-nav">
		<li><a href="#section1">about</a></li>
		<li><a href="#section2">experience</a></li>
		<li><a href="#section3">education</a></li>
		<li><a href="#section4">let's chat</a></li>
		<li><a id="top" href="#">top</a></li>
	</ul>
</nav>
```
### Experiences
Captured in `<section id="section2">` tag

### Projects
Follows after each experience section.
Project gallery contains code like this:
```
<ul class="folio-list" data-img-aspect-ratio="2">
	<!-- Project 1 -->
	<li class="col-xs-10 col-xs-offset-1 col-sm-5 col-sm-offset-1 col-lg-5 col-lg-offset-1">
		<a class="lightbox" href="images/portfolio/project5.jpg">
			<div class="atvImg">
				<img src="images/portfolio/project5.jpg" alt="portfolio">

				<div class="atvImg-layer" data-img="images/portfolio/project5.jpg"></div>
			</div>
		</a>
	</li>

	<!-- Project 2 -->
	<li class="col-xs-10 col-xs-offset-1 col-sm-5 col-sm-offset-0 col-lg-5">
		<a class="lightbox" href="images/portfolio/project5.jpg">
			<div class="atvImg">
				<img src="images/portfolio/project5.jpg" alt="portfolio">

				<div class="atvImg-layer" data-img="images/portfolio/project5.jpg"></div>
			</div>
		</a>
	</li>
</ul>
```
Image ratio can be defined in the `<ul>` tag with this attribute `data-img-aspect-ratio="2"`

*i.e. 2 means WxH = 2x1, 1 means WxH = 1x1, etc.*

Recommended size for ratio 2: **740x370**

### Education
Captured in `<section id="section3">` tag.

Education follows very similar patterns as Experiences section minus the project galleries

### Everything Else
The HTML markups are fairly straight forward, and there are sufficient inline comments to guide you.

---
---
## Dev Notes
### Install NodeJS
https://nodejs.org/en/
### Fetch code from GIT (In console or Git Bash)
`git clone https://github.com/shan-du/dx-portfolio.git`
### Install npm Packages & Dependencies
This includes all required dev packages such as Grunt, LESS, Watch, etc.
```
> npm install
> npm install matchdep
> npm install -g grunt-cli
```

### Start Local Dev
```
// Only watch for file changes
> grunt watch

// Only compile LESS
> grunt less

// Start local f/e server
> grunt server
```
