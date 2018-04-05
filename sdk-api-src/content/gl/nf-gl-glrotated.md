---
UID: NF:gl.glRotated
title: glRotated function
author: windows-driver-content
description: The glRotated function multiplies the current matrix by a rotation matrix.
old-location: opengl\glrotated.htm
old-project: OpenGL
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glRotated, glRotated, glRotated function [OpenGL], opengl.glrotated
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
-	glRotated
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glRotated function


## -description


The <b>glRotated</b> function multiplies the current matrix by a rotation matrix.


## -parameters




### -param angle

The angle of rotation, in degrees.


### -param x

The <i>x</i> coordinate of a vector.


### -param y

The <i>y</i> coordinate of a vector.


### -param z

The <i>z</i> coordinate of a vector.


## -returns



This function does not return a value.




## -remarks



The <b>glRotated</b> function computes a matrix that performs a counterclockwise rotation of <i>angle</i> degrees about the vector from the origin through the point (<i>x</i>, <i>y</i>, <i>z</i>).

The current matrix (see <a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>) is multiplied by this rotation matrix, with the product replacing the current matrix. That is, if M is the current matrix and R is the translation matrix, then M is replaced with M • R.

If the matrix mode is either GL_MODELVIEW or GL_PROJECTION, all objects drawn after <b>glRotated</b> is called are rotated. Use <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a> to save and restore the unrotated coordinate system.

The following functions retrieve information related to <b>glRotated</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_RENDER_MODE


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MODELVIEW_MATRIX


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_PROJECTION_MATRIX


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_TEXTURE_MATRIX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>



<a href="https://msdn.microsoft.com/4c7e5598-534d-4b81-bb58-2e89d0dbfc77">glScale</a>



<a href="https://msdn.microsoft.com/7aa8dc2c-c353-48d3-88a9-389521bed7c9">glTranslate</a>
 

 

