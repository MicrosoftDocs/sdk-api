---
UID: NF:glu.gluPickMatrix
title: gluPickMatrix function
author: windows-driver-content
description: The gluPickMatrix function defines a picking region.
old-location: opengl\glupickmatrix.htm
old-project: OpenGL
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluPickMatrix, glu/gluPickMatrix, gluPickMatrix, gluPickMatrix function [OpenGL], opengl.glupickmatrix"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: glu.h
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
-	glu32.dll
api_name:
-	gluPickMatrix
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluPickMatrix function


## -description


The <b>gluPickMatrix</b> function defines a picking region.


## -parameters




### -param x

The x window coordinate of a picking region.


### -param y

The y window coordinate of a picking region.


### -param width

The width of the picking region in window coordinates.


### -param height

The height of the picking region in window coordinates.


### -param viewport

The current viewport (as from a <a href="https://msdn.microsoft.com/16b04af6-5da3-439f-8d4f-bc8ab1fcb2c5">glGetIntegerv</a> call).


## -returns



This function does not return a value.




## -remarks



The <b>gluPickMatrix</b> function creates a projection matrix you can use to restrict drawing to a small region of the viewport.

<ol>
<li>Use <b>gluPickMatrix</b> to restrict drawing to a small region around the cursor.</li>
<li>Enter selection mode (with <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>), and then rerender the scene.All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.

</li>
</ol>
The matrix created by <b>gluPickMatrix</b> is multiplied by the current matrix just as if <a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a> were called with the generated matrix.

<ol>
<li>Call <a href="https://msdn.microsoft.com/59273aa9-4db3-4c8c-8364-f54c03d2f97a">glLoadIdentity</a> to load an identity matrix onto the perspective matrix stack.</li>
<li>Call <b>gluPickMatrix</b>.</li>
<li>Call a function (such as <a href="https://msdn.microsoft.com/125e2828-a2d7-4c6c-9370-eb21a581ced8">gluPerspective</a>) to multiply the perspective matrix by the pick matrix.</li>
</ol>
When using <b>gluPickMatrix</b> to pick Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>), be careful to turn off the NURBS property, GLU_AUTO_LOAD_MATRIX. If GLU_AUTO_LOAD_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.


#### Examples

When rendering a scene as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */</pre>
</td>
</tr>
</table></span></div>
the following code selects a portion of the viewport: 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/16b04af6-5da3-439f-8d4f-bc8ab1fcb2c5">glGetIntegerv</a>



<a href="https://msdn.microsoft.com/59273aa9-4db3-4c8c-8364-f54c03d2f97a">glLoadIdentity</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>



<a href="https://msdn.microsoft.com/125e2828-a2d7-4c6c-9370-eb21a581ced8">gluPerspective</a>
 

 

