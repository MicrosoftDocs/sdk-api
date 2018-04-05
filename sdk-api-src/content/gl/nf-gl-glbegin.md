---
UID: NF:gl.glBegin
title: glBegin function
author: windows-driver-content
description: The glBegin and glend functions delimit the vertices of a primitive or a group of like primitives.
old-location: opengl\glbegin.htm
old-project: OpenGL
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_LINES, GL_LINE_LOOP, GL_LINE_STRIP, GL_POINTS, GL_POLYGON, GL_QUADS, GL_QUAD_STRIP, GL_TRIANGLES, GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, gl/glBegin, glBegin, glBegin function [OpenGL], opengl.glbegin
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
-	Opengl32.dll
api_name:
-	glBegin
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glBegin function


## -description


The <b>glBegin</b> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a> functions delimit the vertices of a primitive or a group of like primitives.


## -parameters




### -param mode

The primitive or primitives that will be created from vertices presented between <b>glBegin</b> and the subsequent <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a>. The following are accepted symbolic constants and their meanings:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_POINTS"></a><a id="gl_points"></a><dl>
<dt><b>GL_POINTS</b></dt>
</dl>
</td>
<td width="60%">
Treats each vertex as a single point. Vertex <i>n</i> defines point <i>n</i>. <i>N</i> points are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINES"></a><a id="gl_lines"></a><dl>
<dt><b>GL_LINES</b></dt>
</dl>
</td>
<td width="60%">
Treats each pair of vertices as an independent line segment. Vertices <i>2n - 1</i> and <i>2n</i> define line <i>n</i>. <i>N/2</i> lines are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_STRIP"></a><a id="gl_line_strip"></a><dl>
<dt><b>GL_LINE_STRIP</b></dt>
</dl>
</td>
<td width="60%">
Draws a connected group of line segments from the first vertex to the last. Vertices <i>n</i> and <i>n+1</i> define line <i>n</i>. <i>N - 1</i> lines are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_LOOP"></a><a id="gl_line_loop"></a><dl>
<dt><b>GL_LINE_LOOP</b></dt>
</dl>
</td>
<td width="60%">
Draws a connected group of line segments from the first vertex to the last, then back to the first. Vertices <i>n</i> and <i>n + 1</i> define line <i>n</i>. The last line, however, is defined by vertices <i>N</i> and <i>1</i>. <i>N</i> lines are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TRIANGLES"></a><a id="gl_triangles"></a><dl>
<dt><b>GL_TRIANGLES</b></dt>
</dl>
</td>
<td width="60%">
Treats each triplet of vertices as an independent triangle. Vertices <i>3n - 2</i>, <i>3n - 1</i>, and <i>3n</i> define triangle <i>n</i>. <i>N/3</i> triangles are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TRIANGLE_STRIP"></a><a id="gl_triangle_strip"></a><dl>
<dt><b>GL_TRIANGLE_STRIP</b></dt>
</dl>
</td>
<td width="60%">
Draws a connected group of triangles. One triangle is defined for each vertex presented after the first two vertices. For odd <i>n</i>, vertices <i>n</i>, <i>n + 1</i>, and <i>n + 2</i> define triangle <i>n</i>. For even <i>n</i>, vertices <i>n + 1</i>, <i>n</i>, and <i>n + 2</i> define triangle <i>n</i>. <i>N - 2</i> triangles are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TRIANGLE_FAN"></a><a id="gl_triangle_fan"></a><dl>
<dt><b>GL_TRIANGLE_FAN</b></dt>
</dl>
</td>
<td width="60%">
Draws a connected group of triangles. one triangle is defined for each vertex presented after the first two vertices. Vertices <i>1</i>, <i>n + 1</i>, <i>n + 2</i> define triangle <i>n</i>. <i>N - 2</i> triangles are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_QUADS"></a><a id="gl_quads"></a><dl>
<dt><b>GL_QUADS</b></dt>
</dl>
</td>
<td width="60%">
Treats each group of four vertices as an independent quadrilateral. Vertices <i>4n - 3</i>, <i>4n - 2</i>, <i>4n - 1</i>, and <i>4n</i> define quadrilateral <i>n</i>. <i>N/4</i> quadrilaterals are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_QUAD_STRIP"></a><a id="gl_quad_strip"></a><dl>
<dt><b>GL_QUAD_STRIP</b></dt>
</dl>
</td>
<td width="60%">
Draws a connected group of quadrilaterals. One quadrilateral is defined for each pair of vertices presented after the first pair. Vertices <i>2n - 1</i>, <i>2n</i>, <i>2n + 2</i>, and <i>2n + 1</i> define quadrilateral <i>n</i>. <i>N/2 - 1</i> quadrilaterals are drawn. Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON"></a><a id="gl_polygon"></a><dl>
<dt><b>GL_POLYGON</b></dt>
</dl>
</td>
<td width="60%">
Draws a single, convex polygon. Vertices <i>1</i> through <i>N</i> define this polygon.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glBegin</b> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a> functions delimit the vertices that define a primitive or a group of like primitives. The <b>glBegin</b> function accepts a single argument that specifies which of ten primitives the vertices compose. Taking <i>n</i> as an integer count starting at one, and <i>N</i> as the total number of vertices specified, the interpretations are as follows:

<ul>
<li>You can use only a subset of OpenGL functions between <b>glBegin</b> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a>. The functions you can use are:
<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
<div> </div>
<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>
<div> </div>
<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>
<div> </div>
<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>
<div> </div>
<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>
<div> </div>
<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>
<div> </div>
<a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint</a>
<div> </div>
<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
<div> </div>
<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>


You can also use <a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a> or <a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a> to execute display lists that include only the preceding functions. If any other OpenGL function is called between <b>glBegin</b> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a>, the error flag is set and the function is ignored.

</li>
<li>Regardless of the value chosen for <i>mode</i> in <b>glBegin</b>, there is no limit to the number of vertices you can define between <b>glBegin</b> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a>. Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn. Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified. The incomplete primitive is ignored; the complete primitives are drawn.</li>
<li>The minimum specification of vertices for each primitive is:
        <table>
<tr>
<th>Minimum number of vertices</th>
<th>
<div> </div>Type of primitive</th>
</tr>
<tr>
<td>1</td>
<td>point</td>
</tr>
<tr>
<td>2</td>
<td>line</td>
</tr>
<tr>
<td>3</td>
<td>triangle</td>
</tr>
<tr>
<td>4</td>
<td>quadrilateral</td>
</tr>
<tr>
<td>3</td>
<td>polygon</td>
</tr>
</table>
 

</li>
<li>Modes that require a certain multiple of vertices are GL_LINES (2), GL_TRIANGLES (3), GL_QUADS (4), and GL_QUAD_STRIP (2).</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>



<a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>



<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>



<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
 

 

