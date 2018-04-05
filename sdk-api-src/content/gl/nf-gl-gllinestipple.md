---
UID: NF:gl.glLineStipple
title: glLineStipple function
author: windows-driver-content
description: The glLineStipple function specifies the line stipple pattern.
old-location: opengl\gllinestipple.htm
old-project: OpenGL
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glLineStipple, gl/glLineStipple, glLineStipple, glLineStipple function [OpenGL], opengl.gllinestipple"
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
-	glLineStipple
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLineStipple function


## -description


The <b>glLineStipple</b> function specifies the line stipple pattern.


## -parameters




### -param factor

A multiplier for each bit in the line stipple pattern. If <i>factor</i> is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used. The <i>factor</i> parameter is clamped to the range [1, 256] and defaults to one.


### -param pattern

A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized. Bit zero is used first, and the default pattern is all ones.


## -returns



This function does not return a value.




## -remarks



The <b>glLineStipple</b> function specifies the line stipple pattern. Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn. The masking is achieved by using three parameters: the 16-bit line stipple pattern <i>pattern</i>, the repeat count <i>factor</i>, and an integer stipple counter <i>s</i>.

Counter <i>s</i> is reset to zero whenever <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> is called, and before each line segment of a <b>glBegin</b>(GL_LINES)/<b>glEnd</b> sequence is generated. It is incremented after each fragment of a unit width aliased line segment is generated, or after each <i>i</i> fragments of an <i>i</i> width line segment are generated. The <i>i</i> fragments associated with count <i>s</i> are masked out if <i>pattern</i> bit (<i>s</i> / <i>factor</i>) mod 16 is zero. Otherwise these fragments are sent to the framebuffer. Bit zero of <i>pattern</i> is the least significant bit.

Antialiased lines are treated as a sequence of 1x<i>width</i> rectangles for purposes of stippling. Rectangle <i>s</i> is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.

Line stippling is enabled or disabled using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> with argument GL_LINE_STIPPLE. When enabled, the line stipple pattern is applied as described above. When disabled, it is as if the pattern were all ones. Initially, line stippling is disabled.

The following functions retrieve information related to <b>glLineStipple</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LINE_STIPPLE_PATTERN

<b>glGet</b> with argument GL_LINE_STIPPLE_REPEAT


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_LINE_STIPPLE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>



<a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>
 

 

