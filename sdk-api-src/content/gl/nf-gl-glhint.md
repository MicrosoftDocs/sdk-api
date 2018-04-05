---
UID: NF:gl.glHint
title: glHint function
author: windows-driver-content
description: The glHint function specifies implementation-specific hints.
old-location: opengl\glhint.htm
old-project: OpenGL
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_DONT_CARE, GL_FASTEST, GL_FOG_HINT, GL_LINE_SMOOTH_HINT, GL_NICEST, GL_PERSPECTIVE_CORRECTION_HINT, GL_POINT_SMOOTH_HINT, GL_POLYGON_SMOOTH_HINT, _ogl_glHint, gl/glHint, glHint, glHint function [OpenGL], opengl.glhint
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
-	glHint
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glHint function


## -description


The <b>glHint</b> function specifies implementation-specific hints.


## -parameters




### -param target

A symbolic constant indicating the behavior to be controlled. The following symbolic constants, along with suggested semantics, are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_HINT"></a><a id="gl_fog_hint"></a><dl>
<dt><b>GL_FOG_HINT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the accuracy of fog calculation. If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL_DONT_CARE or GL_FASTEST can result in per-vertex calculation of fog effects.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_SMOOTH_HINT"></a><a id="gl_line_smooth_hint"></a><dl>
<dt><b>GL_LINE_SMOOTH_HINT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the sampling quality of antialiased lines. Hinting GL_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PERSPECTIVE_CORRECTION_HINT"></a><a id="gl_perspective_correction_hint"></a><dl>
<dt><b>GL_PERSPECTIVE_CORRECTION_HINT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the quality of color and texture coordinate interpolation. If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL_DONT_CARE or GL_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SMOOTH_HINT"></a><a id="gl_point_smooth_hint"></a><dl>
<dt><b>GL_POINT_SMOOTH_HINT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the sampling quality of antialiased points. Hinting GL_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_SMOOTH_HINT"></a><a id="gl_polygon_smooth_hint"></a><dl>
<dt><b>GL_POLYGON_SMOOTH_HINT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the sampling quality of antialiased polygons. Hinting GL_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.

</td>
</tr>
</table>
 


### -param mode

A symbolic constant indicating the desired behavior. The following symbolic constants are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_FASTEST"></a><a id="gl_fastest"></a><dl>
<dt><b>GL_FASTEST</b></dt>
</dl>
</td>
<td width="60%">
The most efficient option should be chosen.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NICEST"></a><a id="gl_nicest"></a><dl>
<dt><b>GL_NICEST</b></dt>
</dl>
</td>
<td width="60%">
The most correct, or highest quality, option should be chosen.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DONT_CARE"></a><a id="gl_dont_care"></a><dl>
<dt><b>GL_DONT_CARE</b></dt>
</dl>
</td>
<td width="60%">
The client doesn't have a preference.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints. You specify a hint with two arguments. The <i>target</i> parameter is a symbolic constant indicating the behavior to be controlled, and <i>mode</i> is another symbolic constant indicating the desired behavior.

Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.

The <b>glHint</b> function can be ignored.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>
 

 

