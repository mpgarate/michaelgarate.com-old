$(document).ready(function() {
	
	redrawDotNav();
	
	/* Scroll event handler */
    $(window).bind('scroll',function(e){
    	parallaxScroll();
		redrawDotNav();
    });
    
	/* Next/prev and primary nav btn click handlers */
	$('a.web').click(function(){
    	$('html, body').animate({
    		scrollTop:0
    	}, 1000, function() {
	    	parallaxScroll(); // Callback is required for iOS
		});
    	return false;
	});
    $('a.portfolio').click(function(){
    	$('html, body').animate({
    		scrollTop:$('#portfolio').offset().top
    	}, 1000, function() {
	    	parallaxScroll(); // Callback is required for iOS
		});
    	return false;
    });
    $('a.photography').click(function(){
    	$('html, body').animate({
    		scrollTop:$('#photography').offset().top
    	}, 1000, function() {
	    	parallaxScroll(); // Callback is required for iOS
		});
    	return false;
    });
    $('a.motion').click(function(){
    	$('html, body').animate({
    		scrollTop:$('#motion').offset().top
    	}, 1000, function() {
	    	parallaxScroll(); // Callback is required for iOS
		});
    	return false;
    });
	$('a.contact').click(function(){
    	$('html, body').animate({
    		scrollTop:$('#contact').offset().top
    	}, 1000, function() {
	    	parallaxScroll(); // Callback is required for iOS
		});
    	return false;
    });
    
    /* Show/hide dot lav labels on hover */
    $('nav#primary a').hover(
    	function () {
			$(this).prev('h1').show();
		},
		function () {
			$(this).prev('h1').hide();
		}
    );
    
});

/* Scroll the background layers */
function parallaxScroll(){
	var scrolled = $(window).scrollTop();
	$('#parallax-bg1').css('top',(0-(scrolled*.25))+'px');
	$('#parallax-bg2').css('top',(0-(scrolled*.5))+'px');
	$('#parallax-bg3').css('top',(0-(scrolled*.75))+'px');
}

/* Set navigation dots to an active state as the user scrolls */
function redrawDotNav(){
	var section1Top =  0;
	// The top of each section is offset by half the distance to the previous section.
	var section2Top =  $('#portfolio').offset().top - (($('#photography').offset().top - $('#portfolio').offset().top) / 2);
	var section3Top =  $('#photography').offset().top - (($('#motion').offset().top - $('#photography').offset().top) / 2);
	var sectionmTop =  $('#motion').offset().top - (($('#contact').offset().top - $('#motion').offset().top) / 2);
	var section4Top =  $('#contact').offset().top - (($(document).height() - $('#contact').offset().top) / 2);;
	$('nav#primary a').removeClass('active');
	if($(document).scrollTop() >= section1Top && $(document).scrollTop() < section2Top){
		$('nav#primary a.web').addClass('active');
	} else if ($(document).scrollTop() >= section2Top && $(document).scrollTop() < section3Top){
		$('nav#primary a.portfolio').addClass('active');
	} else if ($(document).scrollTop() >= section3Top && $(document).scrollTop() < sectionmTop){
		$('nav#primary a.photography').addClass('active');
	} else if ($(document).scrollTop() >= sectionmTop && $(document).scrollTop() < section4Top){
		$('nav#primary a.motion').addClass('active');
	} else if ($(document).scrollTop() >= section4Top){
		$('nav#primary a.contact').addClass('active');
	}
	
}
