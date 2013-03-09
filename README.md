Jquery Tag Cloud Generator Plugin
=================================

This plugin generates a very simple tag cloud based on the weight/strength of the each element.

Usage
-----
Include the script in the head of the HTML page.
	<script type="text/javascript" src="jquery.tagCloudGenerator.js"></script>
	
On document ready call the plugin.
	$(container).generateTagCloud(data, options);

'data' can be a string or a json array of object {tagName: <name>, tagUrl: <clickable URL [Optional]>, tagStrength: <Number of tags in your system>}.
	
Options
-------
*	numberOfLevel: Int (in %)
	Default: 5
	The number of levels of band in the cloud. The number of different font sizes are based on this configuration.
*	perLevelFontDiffPerc: Int (in %)
	Default: 20
	Percentage font size decrease for every level.
*	baseFontSizePerc: Int (in %)
	Default: 100
	The maximum font size for tags in the highest level band. 
	
Generally, baseFontSizePerc=perLevelFontDiffPerc*numberOfLevel.

CSS
---
You can use the '#tagCloudUl', '#tagCloudUl li', '#tagCloudUl label', and '#tagCloudUl a' to style your cloud. A sample CSS is below.
	#tagCloudUl{
		margin:1em 0;
		padding:.5em .5em .5em .5em;
		text-align:center;	
		background: #ffd65e; /* Old browsers */
		background: -moz-linear-gradient(top, #ffd65e 0%, #febf04 100%); /* FF3.6+ */
		background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,#ffd65e), color-stop(100%,#febf04)); /* Chrome,Safari4+ */
		background: -webkit-linear-gradient(top, #ffd65e 0%,#febf04 100%); /* Chrome10+,Safari5.1+ */
		background: -o-linear-gradient(top, #ffd65e 0%,#febf04 100%); /* Opera 11.10+ */
		background: -ms-linear-gradient(top, #ffd65e 0%,#febf04 100%); /* IE10+ */
		background: linear-gradient(to bottom, #ffd65e 0%,#febf04 100%); /* W3C */
		filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffd65e', endColorstr='#febf04',GradientType=0 ); /* IE6-9 */			
		-moz-border-radius: 5px; 
		-webkit-border-radius: 5px;				
		border-radius: 5px;				
	}

Live in Action
--------------
The plugin is used at http://sl.bitourea.com/ for displaying the tag cloud on the main page. 

Licensing
---------
Released under MIT license, go ahead and use, modify, distribute as you wish. The license is provided in LICENSE.txt. The license of other libraries used must be used as defined by them. 	
