---
UID: NF:gl.glGetPixelMapuiv
title: glGetPixelMapuiv function
author: windows-driver-content
description: The glGetPixelMapfv, glGetPixelMapuiv, and glGetPixelMapusv functions return the specified pixel map.
old-location: opengl\glgetpixelmapuiv.htm
old-project: OpenGL
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glGetPixelMapuiv, glGetPixelMapuiv, glGetPixelMapuiv function [OpenGL], opengl.glgetpixelmapuiv
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
-	Opengl32.dll
api_name:
-	glGetPixelMapuiv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetPixelMapuiv function


## -description


The <a href="https://msdn.microsoft.com/b09f4799-8e36-4d4f-90d8-4a8ed3d15718">glGetPixelMapfv</a>, <b>glGetPixelMapuiv</b>, and <a href="https://msdn.microsoft.com/68b71f9b-5666-4183-aeb8-4c9f09bc5d9c">glGetPixelMapusv</a> functions return the specified pixel map.


## -parameters




### -param map

The name of the pixel map to return. Accepted values are GL_PIXEL_MAP_I_TO_I, GL_PIXEL_MAP_S_TO_S, GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B, GL_PIXEL_MAP_I_TO_A, GL_PIXEL_MAP_R_TO_R, GL_PIXEL_MAP_G_TO_G, GL_PIXEL_MAP_B_TO_B, and GL_PIXEL_MAP_A_TO_A.


### -param values

Returns the pixel map contents.


## -returns



This function does not return a value.




## -remarks



See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a> for a description of the acceptable values for the <i>map</i> parameter. The <b>glGetPixelMap</b> function returns in <i>values</i> the contents of the pixel map specified in <i>map</i>. Use pixel maps during the execution of <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>, <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, and <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a> to map color indexes, stencil indexes, color components, and depth components to other values.

Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero. Return unsigned integer values are undefined if the map value was not in the range [0,1].

To determine the required size of <i>map</i>, call <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with the appropriate symbolic constant.

If an error is generated, no change is made to the contents of <i>values</i>.

The following functions retrieve information related to <b>glGetPixelMap</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_PIXEL_MAP_I_TO_I_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_S_TO_S_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_R_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_G_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_B_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_A_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_R_TO_R_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_G_TO_G_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_B_TO_B_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_A_TO_A_SIZE

<b>glGet</b> with argument GL_MAX_PIXEL_MAP_TABLE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

