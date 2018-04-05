---
UID: NF:gl.glDepthMask
title: glDepthMask function
author: windows-driver-content
description: The glDepthMask function enables or disables writing into the depth buffer.
old-location: opengl\gldepthmask.htm
old-project: OpenGL
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glDepthMask, gl/glDepthMask, glDepthMask, glDepthMask function [OpenGL], opengl.gldepthmask"
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
-	glDepthMask
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDepthMask function


## -description


The <b>glDepthMask</b> function enables or disables writing into the depth buffer.


## -parameters




### -param flag

Specifies whether the depth buffer is enabled for writing. If <i>flag</i> is zero, depth-buffer writing is disabled. Otherwise, it is enabled. Initially, depth-buffer writing is enabled.


## -returns



This function does not return a value.




## -remarks



The following function retrieves information related to <b>glDepthMask</b>:

<b>glGet</b> with argument GL_DEPTH_WRITEMASK




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/23d7f94e-f290-423c-a841-f86caf94009d">glColorMask</a>



<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/f4b5df36-390f-4254-95fb-98589750a11b">glIndexMask</a>



<a href="https://msdn.microsoft.com/c586f9db-bad5-4f06-a194-a8d979842d0c">glStencilMask</a>
 

 

