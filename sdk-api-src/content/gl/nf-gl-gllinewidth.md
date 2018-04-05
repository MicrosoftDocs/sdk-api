---
UID: NF:gl.glLineWidth
title: glLineWidth function
author: windows-driver-content
description: The glLineWidth function specifies the width of rasterized lines.
old-location: opengl\gllinewidth.htm
old-project: OpenGL
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glLineWidth, gl/glLineWidth, glLineWidth, glLineWidth function [OpenGL], opengl.gllinewidth"
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
-	glLineWidth
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLineWidth function


## -description


The <b>glLineWidth</b> function specifies the width of rasterized lines.


## -parameters




### -param width

The width of rasterized lines. The default is 1.0.


## -returns



This function does not return a value.




## -remarks



The <b>glLineWidth</b> function specifies the rasterized width of both aliased and antialiased lines. Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled. Line antialiasing is controlled by calling <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> with argument GL_LINE_SMOOTH.

If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer. (If the rounding results in the value 0.0, it is as if the line width were 1.0) If | Δ x | ≥ | Δ y |, <i>i</i> pixels are filled in each column that is rasterized, where <i>i</i> is the rounded value of <i>width</i>. Otherwise, <i>i</i> pixels are filled in each row that is rasterized.

If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment. The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square. This value is saved and used in the final rasterization step.

Not all widths can be supported when line antialiasing is enabled. If an unsupported width is requested, the nearest supported width is used. Only width 1.0 is guaranteed to be supported; others depend on the implementation. The range of supported widths and the size difference between supported widths within the range can be queried by calling <b>glGet</b> with arguments GL_LINE_WIDTH_RANGE and GL_LINE_WIDTH_GRANULARITY.

The line width specified by <b>glLineWidth</b> is always returned when GL_LINE_WIDTH is queried. Clamping and rounding for aliased and antialiased lines have no effect on the specified value.

Non-antialiased line width may be clamped to an implementation-dependent maximum. Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.

The following functions retrieve information related to <b>glLineWidth</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LINE_WIDTH

<b>glGet</b> with argument GL_LINE_WIDTH_RANGE

<b>glGet</b> with argument GL_LINE_WIDTH_GRANULARITY


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_LINE_SMOOTH




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

