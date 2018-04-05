---
UID: NF:gl.glClipPlane
title: glClipPlane function
author: windows-driver-content
description: The glClipPlane function specifies a plane against which all geometry is clipped.
old-location: opengl\glclipplane.htm
old-project: OpenGL
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glClipPlane, gl/glClipPlane, glClipPlane, glClipPlane function [OpenGL], opengl.glclipplane"
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
-	glClipPlane
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glClipPlane function


## -description


The <b>glClipPlane</b> function specifies a plane against which all geometry is clipped.


## -parameters




### -param plane

The clipping plane that is being positioned. Symbolic names of the form GL_CLIP_PLANE<i>i</i>, where <i>i</i> is an integer between 0 and GL_MAX_CLIP_PLANES - 1, are accepted.


### -param equation

The address of an array of four double-precision floating-point values. These values are interpreted as a plane equation.


## -returns



This function does not return a value.




## -remarks



Geometry is always clipped against the boundaries of a six-plane frustum in <i>x</i>, <i>y</i>, and <i>z</i>. The <b>glClipPlane</b> function allows the specification of additional planes, not necessarily perpendicular to the <i>x-</i>axis, <i>y-</i>axis, or <i>z</i>-axis, against which all geometry is clipped. Up to GL_MAX_CLIP_PLANES planes can be specified, where GL_MAX_CLIP_PLANES is at least six in all implementations. Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.

The <b>glClipPlane</b> function specifies a half-space using a four-component plane equation. When you call <b>glClipPlane</b>,<i>equation</i> is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates. Subsequent changes to the modelview matrix have no effect on the stored plane-equation components. If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane. Otherwise, it is out.

Use the <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> functions to enable and disable clipping planes. Call clipping planes with the argument GL_CLIP_PLANE<i>i</i>, where <i>i</i> is the plane number.

By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.

It is always the case that GL_CLIP_PLANE<i>i</i> = GL_CLIP_PLANE0 + <i>i</i>.

The following functions retrieve information related to <b>glClipPlane</b>:


<a href="https://msdn.microsoft.com/8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6">glGetClipPlane</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_CLIP_PLANE <i>i</i>




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6">glGetClipPlane</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

