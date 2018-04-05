---
UID: NF:gl.glClearIndex
title: glClearIndex function
author: windows-driver-content
description: The glClearIndex function specifies the clear value for the color-index buffers.
old-location: opengl\glclearindex.htm
old-project: OpenGL
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glClearIndex, gl/glClearIndex, glClearIndex, glClearIndex function [OpenGL], opengl.glclearindex"
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
-	glClearIndex
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glClearIndex function


## -description


The <b>glClearIndex</b> function specifies the clear value for the color-index buffers.


## -parameters




### -param c

The index used when the color-index buffers are cleared. The default value is zero.


## -returns



This function does not return a value.




## -remarks



The <b>glClearIndex</b> function specifies the index used by <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> to clear the color-index buffers. The <i>c</i> parameter is not clamped. Rather, <i>c</i> is converted to a fixed-point value with unspecified precision to the right of the binary point. The integer part of this value is then masked with 2<sup>m</sup>  - 1, where <i>m</i> is the number of bits in a color index stored in the framebuffer.

The following functions retrieve information related to <b>glClearIndex</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_INDEX_CLEAR_VALUE

<b>glGet</b> with argument GL_INDEX_BITS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
 

 

