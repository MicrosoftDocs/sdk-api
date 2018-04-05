---
UID: NF:gl.glPointSize
title: glPointSize function
author: windows-driver-content
description: The glPointSize function specifies the diameter of rasterized points.
old-location: opengl\glpointsize.htm
old-project: OpenGL
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glPointSize, gl/glPointSize, glPointSize, glPointSize function [OpenGL], opengl.glpointsize"
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
-	glPointSize
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPointSize function


## -description


The <b>glPointSize</b> function specifies the diameter of rasterized points.


## -parameters




### -param size

The diameter of rasterized points. The default is 1.0.


## -returns



This function does not return a value.




## -remarks



The <b>glPointSize</b> function specifies the rasterized diameter of both aliased and antialiased points. Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled. Point antialiasing is controlled by calling <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> with argument GL_POINT_SMOOTH.

If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer. (If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (<i>x</i>,<i>y</i>) of the pixel fragment that represents the point is computed as

(<i>x</i><sub>w</sub> + .5, <i>y</i><sub>w</sub> + .5)

where <i>w</i> subscripts indicate window coordinates. All pixels that lie within the square grid of the rounded size centered at (<i>x</i>,<i>y</i>) make up the fragment. If the size is even, the center point is

(<i>x</i><sub>w</sub> + .5, <i>y</i><sub>w</sub> + .5)

and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (<i>x</i>,<i>y</i>). All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.

If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (<i>x</i><sub>w</sub> ,<i>y</i><sub>w</sub> ). The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square. This value is saved and used in the final rasterization step. The data associated with each fragment is the data associated with the point being rasterized.

Not all sizes are supported when point antialiasing is enabled. If an unsupported size is requested, the nearest supported size is used. Only size 1.0 is guaranteed to be supported; others depend on the implementation. The range of supported sizes and the size difference between supported sizes within the range can be queried by calling <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with arguments GL_POINT_SIZE_RANGE and GL_POINT_SIZE_GRANULARITY.

The point size specified by <b>glPointSize</b> is always returned when GL_POINT_SIZE is queried. Clamping and rounding for aliased and antialiased points have no effect on the specified value.

Non-antialiased point size may be clamped to an implementation-dependent maximum. Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.

The following functions retrieve information related to <b>glPointSize</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_POINT_SIZE

<b>glGet</b> with argument GL_POINT_SIZE_RANGE

<b>glGet</b> with argument GL_POINT_SIZE_GRANULARITY


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_POINT_SMOOTH




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

