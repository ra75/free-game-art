
WF Map Icon Library
-------------------

Version 0.0.0



Purpose
=======

The purpose of this library is to server as a place to collect various
icons and symbols used for creating maps over fantansy or other worlds
and places.

A possible idea is also to automatically generate game maps from SVG
maps, by converting icons to suitable entities or other things.


Format
======

The format used is Scalable Vector Graphics (SVG).  This is a vector
graphics format that allows efficient storage, scaling, and mass editing
of large maps.

The icons are just small SVG files that can be imported and inserted in
an SVG tool when creating a map.


Size and Location
=================

Icons should be centered around origo (0,0).  This point is considered
to be the actual position of the object the icon represents.  So a tower
or tree could actually have the base/ root centered at (0,0), and the
rest sticking up above.

The size of icons should be about 32 * 32 SVG units.  An SVG unit is
roughly equivalent to 1 pixel, when rendered without any scaling.

Of course, icons representing bigger things could be bigger, such as a
capital city, or a big tree.  64*64 could be considered a recomended
(although not absolute) upper limit.

Icons that represent many objects, like a patch of forest or a number of
huts can be bigger than this.



Naming Standard
===============

The following naming standards should be used for map icons:

<name>_<set>_<instance>_<style>_<author>.svg

   * _name_     is a name for the icon, such as small_hut
   * _set_      indicates that this is a picture with many elements,
                such as many trees or huts, used when creating things
                like a wood or city view. 
   * _instance_ is an instance number.  Each icon may have one or more instances
                that each have a slightly different appearance.
                This way it is possible to avoid repeating patterns when
		creating things like a wood or a village with many huts.
   * _style_    The style this icon is in.  All icons within a style
		should fit together well style wise.  The current styles
		are listed below. 
   * _author_   This is a two or three letter inital for the author.
		This is used to make sure filenames are unique, and to
		indicate the author in an easy way.  Each author along
		with the initials usedby him/her should also be listed
		in the authors file. 

Examples:
~~~~~~~~~
   dark_castle_1_fancy_hh.svg
   conifer_tree_1_symbol_bwh.svg
   conifer_tree_2_symbol_bwh.svg
   hut_set_1_fancy_rms.svg



Styles
======

Currently the following styles are used in the icon library.

If possible new icons should confirm to an existing style.

A single style may contain icons for different map scales.  An overview
map of a country may represent a town as a town icon or star, while a
map of a town can have icons for individual houses, trees, and other
things.


  * fancy

      This is similar in style to icons found in maps in fantasy books,
      such as LotR by Tolkien.

      The icons are seen from diagonally above, and are rather symbolic,
      a town could be represented by four houses inside a wall for
      example.

      Line width should preferably vary a bit, and not be too thin.      

      The icons are colored, but should have overlaying sharp lineart.
      (A line art only map could be generated by removing all colors but
      solid black (#000000) ) The colors should be a bit muted.  A
      standard color palette may be supplied later.

      The light comes from upper left.  Gradients can be used for
      colors, but they shouldn't be too sharp.
 
      
   * symbol

      This is similar to architectural top-down drawings.  Trees are
      represented by circles, houses by rectangles, etc.
  
      Line width is relatively thin (2.0).

      Pale, translucent (about 50%), water color like colors are used.
      No gradients are used.


Scales
======

This is a preliminary set of detail levels, for icons intended to create
maps at different scales.

A detail level describes the types of things that need to be represented
as icons (cities or houses, etc).  A resolution in meters per SVG unit
is also given for icons with more realistic styles, such as the symbol
style.


  * World map

      Cities are represented by things like circles, or circles with
      stars for capitals, etc.  (TODO: not sure if this is needed)

  * Country map

      Cities can be represented as fancy icons with a few prominent
      houses surrounded by a wall, or aerial photograph style, depending
      on the icon style.

  * Area map
 
      A map of a smaller area, like a valley, battlefield, or such.
      Icons for houses are needed, although a small village could still
      be represented by a single icon.

      The scal ecould be around 1 unit per meter.

  * Detail map
     
      Individual houses and trees are separate icons.

      The scale could be around 10 units equals one meter.

  * Indoor map

      Furniture icons and such are needed for this detail level.

      Scale of icons could be around 30 units equals one meter.


TODO: The scale could be indicated by a tag in the filename in the future.




Directory Structure
===================

The directory structure should be kept at one level deep only for now.
Instead of hierarchies like buildings/castles/gothic_castles/ just
castles/ could be used.

   

Contributions
=============

Contributions to this map icon library are welcomed.

If you have a one-time contribution, please email a pointer to it to the
mailing list, and we'll patch it in.  If you wish to participate in an
on-going fashion and demonstrate a willingness to adhere to the
standards on your own, we can provide direct CVS commit access. 


Contacts
========

Discussion about the map library happens on the 

  media@worldforge.org mailing list,

and on the 

  #media IRC channel on irc.worldforge.org.


The library is available from WorldForge CVS at:

  media/map_icons/

For information about how to access CVS and for more information about 
WorldForge, see the FAQ on

  http://www.worldforge.org



