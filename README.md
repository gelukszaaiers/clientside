# clientside
front end of the gelukszaaiers application

## technology
- html5 and css based
- application elements with [React](https://facebook.github.io/react/)
- map magic with [leaflet.js](http://leafletjs.com/)

### a note on the css and html structure
Since March 2017 CSS-grid is supported in most web browsers except IE10/11. This can be tackled with the check for support thanks to this 
new feature in css called _Feature Queries_ (you can find a great tutorial on this on [Youtube by Rachel Andrew](https://www.youtube.com/watch?v=nU0LMoU14n4)): 

'''css
	.someClass{
		//css layout with flexbox or floats or ... 
		//a line with margins and/or widths to fix things
	}
	
	@supports(display: grid){
		//put the changes needed to remove backward compability here
		//grid overrides flexbox, inlineblock, ... but not margins
		.someClass{
			margin: 0;
			width: auto; 
		}
		
	}
'''

CSS grid is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. Making it possible
to have a cleaner html and thus a more easy way to implement React/leaflet/... and to work with components. It keeps the nested div issues away. More info on the
design advantages on CSS grid can be found in this talk on [Youtube by Morten Rand-Hendriksen](https://www.youtube.com/watch?v=7kVeCqQCxlk).