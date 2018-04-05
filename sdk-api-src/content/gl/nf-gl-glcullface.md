---
UID: NF:gl.glCullFace
title: glCullFace function
author: windows-driver-content
description: The glCullFace function specifies whether front-facing or back-facing facets can be culled.
old-location: opengl\glcullface.htm
old-project: OpenGL
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glCullFace, gl/glCullFace, glCullFace, glCullFace function [OpenGL], opengl.glcullface"
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
-	glCullFace
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glCullFace function


## -description


The <b>glCullFace</b> function specifies whether front-facing or back-facing facets can be culled.


## -parameters




### -param mode

Specifies whether front-facing or back-facing facets are candidates for culling. The symbolic constants GL_FRONT, GL_BACK, and GL_FRONT_AND_BACK are accepted. The default value is GL_BACK.


## -returns



This function does not return a value.




## -remarks



The <b>glCullFace</b> function specifies whether front-facing or back-facing facets are culled (as specified by <i>mode</i>) when facet culling is enabled. You enable and disable facet culling using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> with the argument GL_CULL_FACE. Facets include triangles, quadrilaterals, polygons, and rectangles.

The <a href="https://msdn.microsoft.com/4087107c-99cd-4c26-92e3-8dc43633d51f">glFrontFace</a> function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.

If <i>mode</i> is GL_FRONT_AND_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.

The following functions retrieve information related to <b>glCullFace</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_CULL_FACE_MODE


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_CULL_FACE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/4087107c-99cd-4c26-92e3-8dc43633d51f">glFrontFace</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

