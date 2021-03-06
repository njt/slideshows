---
layout: slideshow
title: Practical Visualization Techniques
slides:

    - content: | 
        ## Practical Visualization Techniques

    - content: |

        ## Principles of Visualization (From Tufte)

        * Show the data "truthfully", don't distort it
        * Allow the viewer to understand the most ideas in the shortest time
        * Encourage the viewer to thinking about the form or substance of the data, not the method of display
        * Reveal the structure in the data at a variety of scales
        * Serve a clear purpose within the text or wherever it is displayed
        * Be integrated with other descriptions of the data
        {:.fragment}

      notes: |
        These principles are not absolute, but in general are a good guide to what you should and shouldn't do. They are fairly self explanatory, but here are some notes none the less

        Visualization are made with a message in mind, but that message should be a fair representation of what's in the data, not a distortion or exaggeration of anything present.

        When we are creating a visualization we want the viewing to get the message or idea being displayed quickly as well as conveying a depth of information at the same time. There is generally a trade off between speed of information retrieved by the viewer and the level of information shown.

        The particular method of visualization chosen should be almost transparent to the data, when we look at visualization we are drawn to features of the data, not the method used to display it. 

        [SOMETHING ABOUT SCALE]

        With regard to the last two points, a visualization should be part of whatever piece of media it is displayed in. If it is not stand alone piece, it should be part of and integrate with whatever it's in. It should be clear from a glance what it's prupose is and what it's being used for.

    - content: |
        [Napoleon's March](https://en.wikipedia.org/wiki/Charles_Joseph_Minard#/media/File:Minard.png)
    - content: |
        [Napoleon's March (Translated)](https://upload.wikimedia.org/wikipedia/commons/5/5d/Minard_map_of_napoleon.png)
      notes: |
        Forces visual comparisons (the upper lighter band showing the large army going to Moscow vs. the narrow dark band showing the small army returning).
        Shows causality (the temperature chart at the bottom).
        Captures multivariate complexity (size of army, location, direction, temperature, and time).
        Integrates text and graphic into a coherent whole.
        Illustrate high quality content (complete and accurate data, presented to support Minard’s  argument against war).
        Place comparisons adjacent to each other, not sequentially (people forget if they have to go from page to page ).
        Use the smallest effective differences (i.e., avoid bold colors, heavy lines, distracting labels and scales).

    - content: |
        ## Avoid Chart Junk
        ![alt text](http://1.bp.blogspot.com/-QZRaqE5OK1E/Tyl3KDwofOI/AAAAAAAAAWY/0yyupJsyER8/s1600/F1001E_A_large.gif)
      notes: |

        Hopefully it is clear what chart junk is by looking at this graphic. Chart junk has been a bit of a contentious term; a safe definition is that it's an embliashment that doesnt add anything to the graphic.

        You could argue that this graphic is visually striking, but the embalishments they have used, over lapping pie graphcs and the arrangment of pie graphs across the space of the image, dont add to our understanding of the image, they take away from it. 

        This is a bit of an oversimplification. Its okay to make a graphic "junkier" if you feel it needs to be more striking or memorable. It is a trade off.
    - content: |

        ## Avoid distortion


    - content: |

        ## Encoding with size

        Graphic dimension <= Data dimension
        ![Don't do this](images/purchasing_power.png)


    - content: |
        ## Avoid overplotting



      notes: |
        When we are creating graphs such as scatter and line graphs, we can end up having data that occupies the same space in the chart because the data points are close or identical in value. If our data set is quite large or doest vary much we can end up plotting blobs of indistinguishable data. 

        If we want to continue plotting all the data points we have a few options.

        * Reduce marker size
        * Change marker shape
        * Marker transparency
        * Jitter

        The other options is to change the number of dta points we are plotting. We could do this in a number of ways. We can combine or aggregate the data in some way, using the mean or median for example.

        We could break up the data into sub plots using small muliples (see next slide)

        Or, potenitally you could statistically sample the data and plot the sample.




    - content: |

        ## Small multiples 
        ![Small multiples](http://danmaclean.github.io/content/images/2015/07/small_multiples.png)      

    - content: |

        ## Small multiples
        ![alt text](https://en.wikipedia.org/wiki/Small_multiple#/media/File:The_Horse_in_Motion.jpg)

        Small multiples is a very simple but powerful technique. With small multiples we are taking a data set, and splitting up/disaggregating it by categories we are interested in. 

        In the example shown we have a [] graph, but we are not limited to using only the standard suite of graphs. Small multiples can be used with all varieties of techniques, social network visualizations, maps, whatever. 

        WHen using small multiples, you need to be conscious that each individual graph isn't overtly complicated. Comparisons between each graph become quite diffiuclt otherwise. 

    - content: |
        ## Layering and separating
        ![A simple example of layering](images/stravinsky.png)

    - content: |
        ## Colour rules


      notes: |
        The typical/default colour map or palette used in Scientific Visualization is the rainbow colour map (Red, Orange, Yellow, Green, Blue, Indigo, Violet)

        The big issue with the Rainbow colour map is that it is not perceptually ordered. To remember the ordering most people use a mnemonic Roy G Biv or the like. In studies where people have been asked to place them in order the orderings they come up with vary. If asked to sort a series of shades of grey they place them in order of lightness to darkest, or the reverse. If your data has some sort of ordering, the rainbow colour map wont convent that. 

        Perhaps one advantage of the rainbow colour map is familiarity, people are accustomed to seeing and interpreting it. And it is pretty and quite striking.

        When choosing a colour map here are some principles we should follow

        – The map yields images that are aesthetically pleasing.
        – The map has a maximal perceptual resolution.
        – The order of the colours should be intuitively the same for all people.
        – The perceptual interpolation matches the underlying scalars of the map.
        - distinct for all people, including colour-blind readers;
        - distinct from black and white;
        - distinct on screen and paper;

        From [Kenneth Moreland  ](https://cfwebprod.sandia.gov/cfdocs/CompResearch/docs/ColorMapsExpanded.pdf)

        Here are some tools which can help you pick or create a colour map

        http://colorbrewer2.org/
        https://color.adobe.com/create/color-wheel/
        http://tools.medialab.sciences-po.fr/iwanthue/  
        http://www.mrao.cam.ac.uk/~dag/CUBEHELIX/cubetry.html
        http://paletton.com/

        Matplotlib has changed default colour map, see here for a [talk](https://www.youtube.com/watch?v=xAoljeRJ3lU) on why 
    
    - content: |
        ## The F pattern
        [The F pattern](https://media.nngroup.com/media/editor/alertbox/f_reading_pattern_eyetracking.jpg)
        notes: |
        When we read formatted text (Headings, paragraphs etc) we read it in a F pattern (if we read left to right otherwise it is the reverse. Pictured is a website with a heat map of where users look on the website, from tracking their eyes. The areas most frequently looked at follow a F pattern. This is now a very common pattern for how content is arranged in websites.

        If you have information arranged on the page that want to reader to focus on, you need a way of drawing readers attention to it 

        



    - content: |

        ## Iterate



      notes: |
        You are probably not going to get it right the first time. Creating your figures using script in R/Python etc makes iteration very easy. Changing the various graphical elements of a figure is very quick, and unlike say excel easily revertible, its just code. 

        What makes sense to you wont necessarily make sense to others. Just as you have others read over your work to check that the text flows and is free of errors, the same should be done for graphics you create. Validate your design decisions, particularly on more complex graphics. 

        

        

    - content: |
        ## Aesthetics

      notes: |
        Don't be afraid of spending time to make your graphics look nice beyond the point of a serviceable level of attractiveness. Graphics are not just something you throw into a report and then forget about them. 

         Going beyond this point inst [something], Make graphics that people want to look at. 




    - content: |

        ## Tables

        + If you can effectively convey information with a graph, use a graph

        + Tables still have a place, most often as a reference


    - content: |

        ## General rules for using tables
        * Several smaller tables are better than one large table
        * Structure the table for how your audience will use the data
        * Arrange rows and columns by some sort of context - size, name etc

    - content: | 
        ## Use an Anchor figure
        Hilight the principle data points you want compared to the rest of the data
        ![alt text](http://stats.blogoverflow.com/files/2012/02/table_Feinberg.png)

    - content: | 
        ## Colour lines
        Improves readability remarkably, especially for larger tables
        ![alt text](http://media.24ways.org/2007/07/illi_7.gif)


    - content: | 
        ## Combine Tables and Graphs
        Show trends/patterns in data as well as exact values
        ![alt text](http://www.perceptualedge.com/images/example2improvedsolution.GIF)


    - content: |
        ## Sparklines   
        Show shape and variation of data 
        ![alt text](http://i.stack.imgur.com/C463D.png)

    - content: |
        ## Visualizing high dimensional/ complex data    

        ![alt text](https://c1.staticflickr.com/7/6142/5920564485_d34dbc2549_b.jpg)


    - content: |
        ## Visualizing high dimensional/ complex data  
        ![alt text](https://archinate.files.wordpress.com/2015/05/edu-workshop-tableaupublic-datadriven1.png)

    - content: |
        ## Explore your options, there is a whole [zoo](http://queue.acm.org/detail.cfm?id=1805128) of choices out there
        There might not be an established solution yet  ¯\\_(ツ)_/¯ so be creative
      notes: |
        http://www.visual-literacy.org/periodic_table/periodic_table.html#


---