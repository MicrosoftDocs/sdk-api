---
UID: NF:gl.glFeedbackBuffer
title: glFeedbackBuffer function
author: windows-driver-content
description: The glFeedbackBuffer function controls feedback mode.
old-location: opengl\glfeedbackbuffer.htm
old-project: OpenGL
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glFeedbackBuffer, gl/glFeedbackBuffer, glFeedbackBuffer, glFeedbackBuffer function [OpenGL], opengl.glfeedbackbuffer"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	opengl32.dll
api_name:
-	glFeedbackBuffer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glFeedbackBuffer function


## -description


The <b>glFeedbackBuffer</b> function controls feedback mode.


## -parameters




### -param size

The maximum number of values that can be written into <i>buffer</i>.


### -param type

A symbolic constant that describes the information that will be returned for each vertex. The following symbolic constants are accepted: GL_2D, GL_3D, GL_3D_COLOR, GL_3D_COLOR_TEXTURE, and GL_4D_COLOR_TEXTURE.


### -param buffer

Returns the feedback data.


## -returns



This function does not return a value.




## -remarks



The <b>glFeedbackBuffer</b> function controls feedback. Feedback, like selection, is an OpenGL mode. The mode is selected by calling <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a> with GL_FEEDBACK. When OpenGL is in feedback mode, no pixels are produced by rasterization. Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.

The <b>glFeedbackBuffer</b> function has three arguments:

<ul>
<li><i>buffer</i> is a pointer to an array of floating-point values into which feedback information is placed.</li>
<li><i>size</i> indicates the size of the array.</li>
<li><i>type</i> is a symbolic constant describing the information that is fed back for each vertex.</li>
</ul>
You must issue <b>glFeedbackBuffer</b> before feedback mode is enabled (by calling <b>glRenderMode</b> with argument GL_FEEDBACK). Setting GL_FEEDBACK without establishing the feedback buffer, or calling <b>glFeedbackBuffer</b> while OpenGL is in feedback mode, is an error.

Take OpenGL out of feedback mode by calling <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a> with a parameter value other than GL_FEEDBACK. When you do this while OpenGL is in feedback mode, <b>glRenderMode</b> returns the number of entries placed in the feedback array. The returned value never exceeds <i>size</i>. If the feedback data required more room than was available in <i>buffer</i>, <b>glRenderMode</b> returns a negative value.

While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array. If doing so would cause the number of entries to exceed the maximum, <b>glFeedbackBuffer</b> partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag. Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data. The <b>glFeedbackBuffer</b> function also writes entries for bitmaps and pixel rectangles. Feedback occurs after polygon culling and <a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a> interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer. It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.

You can insert a marker into the feedback buffer with <a href="https://msdn.microsoft.com/14664ac6-eb25-46ae-86d8-7ece31df103f">glPassThrough</a>.

The following is the grammar for the blocks of values written into the feedback buffer. Each primitive is indicated with a unique identifying value followed by some number of vertices. Polygon entries include an integer value indicating how many vertices follow. A vertex is fed back as some number of floating-point values, as determined by <i>type</i>. Colors are fed back as four values in RGBA mode and one value in color-index mode.

feedbackList &lt;— feedbackItem feedbackList | feedbackItem

feedbackItem &lt;— point | lineSegment | polygon | bitmap | pixelRectangle | passThru

point &lt;— GL_POINT_TOKEN vertex

lineSegment &lt;— GL_LINE_TOKEN vertex vertex | GL_LINE_RESET_TOKEN vertex vertex

polygon &lt;— GL_POLYGON_TOKEN n polySpec

polySpec &lt;— polySpec vertex | vertex vertex vertex

bitmap &lt;— GL_BITMAP_TOKEN vertex

pixelRectangle &lt;— GL_DRAW_PIXEL_TOKEN vertex | GL_COPY_PIXEL_TOKEN vertex

passThru &lt;— GL_PASS_THROUGH_TOKEN value

vertex &lt;— 2d | 3d | 3dColor | 3dColorTexture | 4dColorTexture

2d &lt;— value value

3d &lt;— value value value

3dColor &lt;— value value value color

3dColorTexture &lt;— value value value color tex

4dColorTexture &lt;— value value value value color tex

color &lt;— rgba | index

rgba &lt;— value value value value

index &lt;— value

tex &lt;— value value value value

The <i>value</i> parameter is a floating-point number, and <i>n</i> is a floating-point integer giving the number of vertices in the polygon. The following are symbolic floating-point constants: GL_POINT_TOKEN, GL_LINE_TOKEN, GL_LINE_RESET_TOKEN, GL_POLYGON_TOKEN, GL_BITMAP_TOKEN, GL_DRAW_PIXEL_TOKEN, GL_COPY_PIXEL_TOKEN, and GL_PASS_THROUGH_TOKEN. GL_LINE_RESET_TOKEN is returned whenever the line stipple pattern is reset. The data returned as a vertex depends on the feedback <i>type</i>.

The following table gives the correspondence between <i>type</i> and the number of values per vertex; <i>k</i> is 1 in color-index mode and 4 in RGBA mode.

<table>
<tr>
<th>
<div> </div>Type</th>
<th>
<div> </div>Coordinates</th>
<th>
<div> </div>Color</th>
<th>
<div> </div>Texture</th>
<th>Total number of values</th>
</tr>
<tr>
<td>GL_2D</td>
<td><i>x</i>, <i>y</i></td>
<td></td>
<td></td>
<td>2</td>
</tr>
<tr>
<td>GL_3D</td>
<td><i>x</i>, <i>y</i>, <i>z</i></td>
<td></td>
<td></td>
<td>3</td>
</tr>
<tr>
<td>GL_3D_COLOR</td>
<td><i>x</i>, <i>y</i>, <i>z</i></td>
<td><i>k</i></td>
<td></td>
<td>3 + <i>k</i></td>
</tr>
<tr>
<td>GL_3D_COLOR_TEXTURE</td>
<td><i>x</i>, <i>y</i>, <i>z</i>,</td>
<td><i>k</i></td>
<td>4</td>
<td>7 + <i>k</i></td>
</tr>
<tr>
<td>GL_4D_COLOR_TEXTURE</td>
<td><i>x</i>, <i>y</i>, <i>z</i>, <i>w</i></td>
<td><i>k</i></td>
<td>4</td>
<td>8 + <i>k</i></td>
</tr>
</table>
 

Feedback vertex coordinates are in window coordinates, except <i>w</i>, which is in clip coordinates. Feedback colors are lighted, if lighting is enabled. Feedback texture coordinates are generated, if texture coordinate generation is enabled. They are always transformed by the texture matrix.

The <b>glFeedbackBuffer</b> function, when used in a display list, is not compiled into the display list but rather is executed immediately.

The following function retrieves information related to <b>glFeedbackBuffer</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_RENDER_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>



<a href="https://msdn.microsoft.com/14664ac6-eb25-46ae-86d8-7ece31df103f">glPassThrough</a>



<a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>



<a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>



<a href="https://msdn.microsoft.com/b5c64364-1f47-4281-96b5-95c3f5c8e753">glSelectBuffer</a>
 

 

