---
UID: NF:gl.glReadBuffer
title: glReadBuffer function
author: windows-driver-content
description: The glReadBuffer function selects a color buffer source for pixels.
old-location: opengl\glreadbuffer.htm
old-project: OpenGL
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glReadBuffer, gl/glReadBuffer, glReadBuffer, glReadBuffer function [OpenGL], opengl.glreadbuffer"
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
-	glReadBuffer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glReadBuffer function


## -description


The <b>glReadBuffer</b> function selects a color buffer source for pixels.


## -parameters




### -param mode

A color buffer. Accepted values are GL_FRONT_LEFT, GL_FRONT_RIGHT, GL_BACK_LEFT, GL_BACK_RIGHT, GL_FRONT, GL_BACK, GL_LEFT, GL_RIGHT, and GL_AUX <i>i</i>, where <i>i</i> is between 0 and GL_AUX_BUFFERS 1.


## -returns



This function does not return a value.




## -remarks



The <b>glReadBuffer</b> function specifies a color buffer as the source for subsequent <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a> and <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a> commands. The <i>mode</i> parameter accepts one of twelve or more predefined values. (GL_AUX0 through GL_AUX3 are always defined.) In a fully configured system, GL_FRONT, GL_LEFT, and GL_FRONT_LEFT all name the front-left buffer, GL_FRONT_RIGHT and GL_RIGHT name the front-right buffer, and GL_BACK_LEFT and GL_BACK name the back-left buffer.

Nonstereo double-buffered configurations have only a front-left and a back-left buffer. Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo. It is an error to specify a nonexistent buffer to <b>glReadBuffer</b>.

By default, <i>mode</i> is GL_FRONT in single-buffered configurations, and GL_BACK in double-buffered configurations.

The following function retrieves information related to <b>glReadBuffer</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_READ_BUFFER




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>
 

 

