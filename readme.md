Python program to clean up SVG files, particularly those created by Inkscape or Illustrator

# --- Current Functionality ---

## Remove attributes
	Remove attributes with a given name, e.g. remove 'id' attributes, which often aren't used.

## Remove namespaces
	Remove all attributes associated with a given namespace, e.g. remove 'sodipodi' attributes created by Inkscape.

## Set decimal places
    Rewrite attributes to a given number of decimal places.
    Strip out unnecessary trailing zeros.
    
* Attributes
	- x, y, x1, y2, x2, y2
	- cx, cy
	- r, rx, ry
	- width, height
	- points
	- d

## Apply transformations
	Applies transformations to elements so the attribute can be removed.

* Translation
    - In the form
        - comma: (12,34)
        - space(s): (12 34)
        - comma and space(s): (12, 34), (12 ,34), (12 , 34)
        - decimal: (1.2, 3.4)
        - negative: (-1.2, -3.4)
        
    - Shapes
        - line
        - rect
        - circle, ellipse
        - polyline, polygon
        - path (not fully tested)

## CSS stlying
    Convert individual style attributes to CSS styling.
    Remove default styles.
    
# --- To Do ---

## Transformations

* Translation
    - In the form
        - single: (12)

    - Shapes
        - g
        - text
        - tspan
        
* Rotation
    - Shapes
        - path
        - polyline/polygon
        - line
        - circle
        - rect -> polygon/path?
        
* Scale
    - Shapes
        - path
        - polyline/polygon
        - line
        - rect
        - circle -> ellipse?
        
* SkewX and SkewY
	- Shapes
		- line
		- path
		- polyline/polygon
		- rect -> polygon/path?
		- circle -> path arc?
		
* Matrix
	- Shapes
		- line
		- path
		- polyline/polygon
		- rect -> polygon/path?
            
## CSS stlying
	Need to check whether style element already exists and whether class names already exist.
    Ideally find most efficient way to class elements for styling.
    
## Flatten groups
	Remove groups that aren't adding properties, such as animations or transforms
