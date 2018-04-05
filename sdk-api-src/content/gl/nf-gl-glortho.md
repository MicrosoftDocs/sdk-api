---
UID: NF:gl.glOrtho
title: glOrtho function
author: windows-driver-content
description: The glOrtho function multiplies the current matrix by an orthographic matrix.
old-location: opengl\glortho.htm
old-project: OpenGL
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glOrtho, gl/glOrtho, glOrtho, glOrtho function [OpenGL], opengl.glortho"
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
-	glOrtho
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glOrtho function


## -description


The <b>glOrtho</b> function multiplies the current matrix by an orthographic matrix.


## -parameters




### -param left

The coordinates for the left vertical clipping plane.


### -param right

The coordinates for theright vertical clipping plane.


### -param bottom

The coordinates for the bottom horizontal clipping plane.


### -param top

The coordinates for the top horizontal clipping plans.


### -param zNear

The distances to the nearer depth clipping plane. This distance is negative if the plane is to be behind the viewer.


### -param zFar

The distances to the farther depth clipping plane. This distance is  negative if the plane is to be behind the viewer.


## -returns



This function does not return a value.




## -remarks



The <b>glOrtho</b> function describes a perspective matrix that produces a parallel projection. The (<i>left</i>, <i>bottom</i>, <i>near</i>) and (<i>right</i>, <i>top</i>, <i>near</i>) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0). The <i>far</i> parameter specifies the location of the far clipping plane. Both <i>zNear</i> and <i>zFar</i> can be either positive or negative. The corresponding matrix is shown in the following image.

<img alt="" border="0" src="images/ortho1.png"/>
where

<img alt="" border="0" src="images/ortho2.png"/>
The current matrix is multiplied by this matrix with the result replacing the current matrix. That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M • O.

Use <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <b>glPopMatrix</b> to save and restore the current matrix stack. Use <a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a> to set the current matrix.

The following functions retrieve information related to <b>glOrtho</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE

<b>glGet</b> with argument GL_MODELVIEW_MATRIX

<b>glGet</b> with argument GL_PROJECTION_MATRIX

<b>glGet</b> with argument GL_TEXTURE_MATRIX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3">glFrustum</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>



<a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>
 

 

