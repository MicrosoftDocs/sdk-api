---
UID: NF:gl.glStencilMask
title: glStencilMask function
author: windows-driver-content
description: The glStencilMask function controls the writing of individual bits in the stencil planes.
old-location: opengl\glstencilmask.htm
old-project: OpenGL
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glStencilMask, gl/glStencilMask, glStencilMask, glStencilMask function [OpenGL], opengl.glstencilmask"
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
-	glStencilMask
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glStencilMask function


## -description


The <b>glStencilMask</b> function controls the writing of individual bits in the stencil planes.


## -parameters




### -param mask

A bit mask to enable and disable writing of individual bits in the stencil planes. Initially, the mask is all ones.


## -returns



This function does not return a value.




## -remarks



The <b>glStencilMask</b> function controls the writing of individual bits in the stencil planes. The least significant <i>n</i> bits of <i>mask</i>, where <i>n</i> is the number of bits in the stencil buffer, specify a mask. Wherever a one appears in the mask, the corresponding bit in the stencil buffer is made writable. Where a zero appears, the bit is write-protected. Initially, all bits are enabled for writing.

The following functions retrieve information related to <b>glStencilMask</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_STENCIL_WRITEMASK

glGet with argument GL_STENCIL_BITS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/23d7f94e-f290-423c-a841-f86caf94009d">glColorMask</a>



<a href="https://msdn.microsoft.com/067b18e2-f21a-4dde-8fa6-dd975746e189">glDepthMask</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/f4b5df36-390f-4254-95fb-98589750a11b">glIndexMask</a>



<a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>
 

 

