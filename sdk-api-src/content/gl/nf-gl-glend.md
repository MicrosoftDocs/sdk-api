---
UID: NF:gl.glEnd
title: glEnd function
author: windows-driver-content
description: The glBegin and glend functions delimit the vertices of a primitive or a group of like primitives.
old-location: opengl\glend.htm
old-project: OpenGL
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glEnd, glEnd, glEnd function [OpenGL], opengl.glend
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
-	glEnd
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEnd function


## -description


The <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <b>glend</b> functions delimit the vertices of a primitive or a group of like primitives.


## -parameters






## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <b>glend</b> functions delimit the vertices that define a primitive or a group of like primitives. The <b>glBegin</b> function accepts a single argument that specifies which of ten primitives the vertices compose. Taking <i>n</i> as an integer count starting at one, and <i>N</i> as the total number of vertices specified, the interpretations are as follows:

<ul>
<li>
You can use only a subset of OpenGL functions between <b>glBegin</b> and <b>glEnd</b>. The functions you can use are:


<ul>
<li>
<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
</li>
<li>
<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>
</li>
<li>
<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
</li>
<li>
<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>
</li>
</ul>


You can also use <a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a> or <a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a> to execute display lists that include only the preceding functions. If any other OpenGL function is called between <b>glBegin</b> and <b>glEnd</b>, the error flag is set and the function is ignored.

</li>
<li>Regardless of the value chosen for <i>mode</i> in <b>glBegin</b>, there is no limit to the number of vertices you can define between <b>glBegin</b> and <b>glEnd</b>. Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn. Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified. The incomplete primitive is ignored; the complete primitives are drawn.</li>
<li>The minimum specification of vertices for each primitive is:
        <table>
<tr>
<th>Minimum number of vertices</th>
<th>Type of primitive</th>
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




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>



<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>



<a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>



<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>



<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
 

 

