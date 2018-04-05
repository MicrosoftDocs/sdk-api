---
UID: NF:gl.glFrontFace
title: glFrontFace function
author: windows-driver-content
description: The glFrontFace function defines front-facing and back-facing polygons.
old-location: opengl\glfrontface.htm
old-project: OpenGL
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glFrontFace, gl/glFrontFace, glFrontFace, glFrontFace function [OpenGL], opengl.glfrontface"
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
-	glFrontFace
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glFrontFace function


## -description


The <b>glFrontFace</b> function defines front-facing and back-facing polygons.


## -parameters




### -param mode

The orientation of front-facing polygons. GL_CW and GL_CCW are accepted. The default value is GL_CCW.


## -returns



This function does not return a value.




## -remarks



In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible. Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image. You enable and disable elimination of back-facing polygons with <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> using argument GL_CULL_FACE.

The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon. The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon. The <b>glFrontFace</b> function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing. Passing GL_CCW to <i>mode</i> selects counterclockwise polygons as front-facing; GL_CW selects clockwise polygons as front-facing. By default, counterclockwise polygons are taken to be front-facing.

The following function retrieves information about <b>glFrontface</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_FRONT_FACE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>
 

 

