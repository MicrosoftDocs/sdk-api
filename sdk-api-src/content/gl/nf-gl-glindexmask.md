---
UID: NF:gl.glIndexMask
title: glIndexMask function
author: windows-driver-content
description: The glIndexMask function controls the writing of individual bits in the color-index buffers.
old-location: opengl\glindexmask.htm
old-project: OpenGL
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glIndexMask, gl/glIndexMask, glIndexMask, glIndexMask function [OpenGL], opengl.glindexmask"
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
-	glIndexMask
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glIndexMask function


## -description


The <b>glIndexMask</b> function controls the writing of individual bits in the color-index buffers.


## -parameters




### -param mask

A bit mask to enable and disable the writing of individual bits in the color-index buffers. Initially, the mask is all ones.


## -returns



This function does not return a value.




## -remarks



The <b>glIndexMask</b> function controls the writing of individual bits in the color-index buffers. The least significant <i>n</i> bits of <i>mask</i>, where <i>1</i> is the number of bits in a color-index buffer, specify a mask. Wherever a one appears in the mask, the corresponding bit in the color-index buffer (or buffers) is made writable. Where a zero appears, the bit is write-protected.

This mask is used only in color-index mode, and it affects only the buffers currently selected for writing (see <a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>). Initially, all bits are enabled for writing.

The following function retrieves information related to <b>glIndexMask</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_INDEX_WRITEMASK




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/067b18e2-f21a-4dde-8fa6-dd975746e189">glDepthMask</a>



<a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>



<a href="https://msdn.microsoft.com/c586f9db-bad5-4f06-a194-a8d979842d0c">glStencilMask</a>
 

 

