---
UID: NF:gl.glDepthRange
title: glDepthRange function
author: windows-driver-content
description: The glDepthRange function specifies the mapping of z values from normalized device coordinates to window coordinates.
old-location: opengl\gldepthrange.htm
old-project: OpenGL
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glDepthRange, gl/glDepthRange, glDepthRange, glDepthRange function [OpenGL], opengl.gldepthrange"
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
-	glDepthRange
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDepthRange function


## -description


The <b>glDepthRange</b> function specifies the mapping of <i>z</i> values from normalized device coordinates to window coordinates.


## -parameters




### -param zNear

The mapping of the near clipping plane to window coordinates. The default value is zero.


### -param zFar

The mapping of the far clipping plane to window coordinates. The default value is 1.


## -returns



This function does not return a value.




## -remarks



After clipping and division by <i>w</i>, <i>z</i> -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes. The <b>glDepthRange</b> function specifies a linear mapping of the normalized <i>z</i>-coordinates in this range to window <i>z</i>-coordinates. Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components). Thus, the values accepted by <b>glDepthRange</b> are both clamped to this range before they are accepted.

The default mapping of (0,1) maps the near plane to 0 and the far plane to 1. With this mapping, the depth buffer range is fully utilized.

It is not necessary that <i>zNear</i> be less than <i>zFar</i>. Reverse mappings such as (1,0) are acceptable.

The following function retrieves information related to <b>glDepthRange</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_DEPTH_RANGE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>
 

 

