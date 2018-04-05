---
UID: NF:gl.glPolygonMode
title: glPolygonMode function
author: windows-driver-content
description: The glPolygonMode function selects a polygon rasterization mode.
old-location: opengl\glpolygonmode.htm
old-project: OpenGL
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_FILL, GL_LINE, GL_POINT, _ogl_glPolygonMode, gl/glPolygonMode, glPolygonMode, glPolygonMode function [OpenGL], opengl.glpolygonmode
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
-	glPolygonMode
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPolygonMode function


## -description


The <b>glPolygonMode</b> function selects a polygon rasterization mode.


## -parameters




### -param face

The polygons that <i>mode</i> applies to. Must be GL_FRONT for front-facing polygons, GL_BACK for back-facing polygons, or GL_FRONT_AND_BACK for front- and back-facing polygons.


### -param mode

The way polygons will be rasterized. The following modes are defined and can be specified in <i>mode</i>. The default is GL_FILL for both front- and back-facing polygons.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_POINT"></a><a id="gl_point"></a><dl>
<dt><b>GL_POINT</b></dt>
</dl>
</td>
<td width="60%">
Polygon vertices that are marked as the start of a boundary edge are drawn as points. Point attributes such as GL_POINT_SIZE and GL_POINT_SMOOTH control the rasterization of the points. Polygon rasterization attributes other than GL_POLYGON_MODE have no effect.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE"></a><a id="gl_line"></a><dl>
<dt><b>GL_LINE</b></dt>
</dl>
</td>
<td width="60%">
Boundary edges of the polygon are drawn as line segments. They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>). Line attributes such as GL_LINE_WIDTH and GL_LINE_SMOOTH control the rasterization of the lines. Polygon rasterization attributes other than GL_POLYGON_MODE have no effect.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FILL"></a><a id="gl_fill"></a><dl>
<dt><b>GL_FILL</b></dt>
</dl>
</td>
<td width="60%">
The interior of the polygon is filled. Polygon attributes such as GL_POLYGON_STIPPLE and GL_POLYGON_SMOOTH control the rasterization of the polygon.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glPolygonMode</b> function controls the interpretation of polygons for rasterization. The <i>face</i> parameter describes which polygons <i>mode</i> applies to: front-facing polygons (GL_FRONT), back-facing polygons (GL_BACK), or both (GL_FRONT_AND_BACK). The polygon mode affects only the final rasterization of polygons. In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.

To draw a surface with filled back-facing polygons and outlined front-facing polygons, call

<b>glPolygonMode</b>(GL_FRONT, GL_LINE);

Vertices are marked as boundary or nonboundary with an edge flag. Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using <a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>.

The following function retrieves information related to <b>glPolygonMode</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_POLYGON_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>



<a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>



<a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>



<a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>
 

 

