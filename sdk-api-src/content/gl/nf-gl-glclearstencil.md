---
UID: NF:gl.glClearStencil
title: glClearStencil function
author: windows-driver-content
description: The glClearStencil function specifies the clear value for the stencil buffer.
old-location: opengl\glclearstencil.htm
old-project: OpenGL
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glClearStencil, gl/glClearStencil, glClearStencil, glClearStencil function [OpenGL], opengl.glclearstencil"
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
-	glClearStencil
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glClearStencil function


## -description


The <b>glClearStencil</b> function specifies the clear value for the stencil buffer.


## -parameters




### -param s

The index used when the stencil buffer is cleared. The default value is zero.


## -returns



This function does not return a value.




## -remarks



The <b>glClearStencil</b> function specifies the index used by <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> to clear the stencil buffer. The <i>s</i> parameter is masked with 2<sup>m</sup>  - 1, where <i>m</i> is the number of bits in the stencil buffer.

The following functions retrieve information related to the <b>glClearStencil</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_STENCIL_CLEAR_VALUE

<b>glGet</b> with argument GL_STENCIL_BITS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
 

 

