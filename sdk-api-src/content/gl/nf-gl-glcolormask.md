---
UID: NF:gl.glColorMask
title: glColorMask function
author: windows-driver-content
description: The glColorMask function enables and disables writing of frame-buffer color components.
old-location: opengl\glcolormask.htm
old-project: OpenGL
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glColorMask, gl/glColorMask, glColorMask, glColorMask function [OpenGL], opengl.glcolormask"
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
-	glColorMask
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glColorMask function


## -description


The <b>glColorMask</b> function enables and disables writing of frame-buffer color components.


## -parameters




### -param red

Specify whether red can or cannot be written into the framebuffer. The default values is GL_TRUE, indicating that the color component can be written. 



### -param green

Specify whether green can or cannot be written into the framebuffer. The default value is GL_TRUE, indicating that the color component can be written. 



### -param blue

Specify whether blue can or cannot be written into the framebuffer. The default value is GL_TRUE, indicating that the color component can be written. 



### -param alpha

Specify whether alpha can or cannot be written into the framebuffer. The default value is GL_TRUE, indicating that the color component can be written. 



## -returns



This function does not return a value.




## -remarks



The <b>glColorMask</b> function specifies whether the individual color components in the framebuffer can or cannot be written. If <i>red</i> is GL_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.

Changes to individual bits of components cannot be controlled. Rather, changes are either enabled or disabled for entire color components.

The following functions retrieve information related to <b>glColorMask</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_COLOR_WRITEMASK

<b>glGet</b> with argument GL_RGBA_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/067b18e2-f21a-4dde-8fa6-dd975746e189">glDepthMask</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">
glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">
glIndex</a>



<a href="https://msdn.microsoft.com/f4b5df36-390f-4254-95fb-98589750a11b">glIndexMask</a>



<a href="https://msdn.microsoft.com/c586f9db-bad5-4f06-a194-a8d979842d0c">glStencilMask</a>
 

 

