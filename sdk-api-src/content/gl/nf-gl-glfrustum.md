---
UID: NF:gl.glFrustum
title: glFrustum function
author: windows-driver-content
description: The glFrustum function multiplies the current matrix by a perspective matrix.
old-location: opengl\glfrustum.htm
old-project: OpenGL
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glFrustum, gl/glFrustum, glFrustum, glFrustum function [OpenGL], opengl.glfrustum"
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
-	glFrustum
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glFrustum function


## -description


The <b>glFrustum</b> function multiplies the current matrix by a perspective matrix.


## -parameters




### -param left

The coordinate for the left-vertical clipping plane.


### -param right

The coordinate for the right-vertical clipping plane.


### -param bottom

The coordinate for the bottom-horizontal clipping plane.


### -param top

The coordinate for the bottom-horizontal clipping plane.		


### -param zNear

The distances to the near-depth clipping plane. Must be positive.


### -param zFar

The distances to the far-depth clipping planes. Must be positive.


## -returns



This function does not return a value.




## -remarks



The <b>glFrustum</b> function describes a perspective matrix that produces a perspective projection. The (<i>left</i>, <i>bottom</i>, <i>zNear</i>) and (<i>right</i>, <i>top</i>, <i>zNear</i>) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0). The <i>zFar</i> parameter specifies the location of the far clipping plane. Both <i>zNear</i> and <i>zFar</i> must be positive. The corresponding matrix is shown in the following image.

<img alt="" border="0" src="images/frust01.png"/>
<img alt="" border="0" src="images/frust02.png"/>
The <b>glFrustum</b> function multiplies the current matrix by this matrix, with the result replacing the current matrix. That is, if M is the current matrix and F is the frustum perspective matrix, then <b>glFrustum</b> replaces M with M • F.

Use <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a> to save and restore the current matrix stack.

Depth-buffer precision is affected by the values specified for <i>zNear</i> and <i>zFar</i>. The greater the ratio of <i>zFar</i> to <i>zNear</i> is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other. If

<img alt="" border="0" src="images/frust03.png"/>
roughly <i>log</i>₂ (<i>r</i>) bits of depth buffer precision are lost. Because <i>r</i> approaches infinity as <i>zNear</i> approaches zero, you should never set <i>zNear</i> to zero.

The following functions retrieve information about <b>glFrustum</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE

<b>glGet</b> with argument GL_MODELVIEW_MATRIX

<b>glGet</b> with argument GL_PROJECTION_MATRIX

<b>glGet</b> with argument GL_TEXTURE_MATRIX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/5c70819f-e9b6-49e2-add5-9f6e6aba26ee">glOrtho</a>



<a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>



<a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>
 

 

