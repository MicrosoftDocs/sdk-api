---
UID: NF:gl.glScalef
title: glScalef function
author: windows-driver-content
description: The glScaled and glScalef functions multiply the current matrix by a general scaling matrix.
old-location: opengl\glscalef.htm
old-project: OpenGL
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glScalef, glScalef, glScalef function [OpenGL], opengl.glscalef
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
-	glScalef
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glScalef function


## -description


The <a href="https://msdn.microsoft.com/3846289f-5c7b-4bb6-95a8-90a58dd8b9d9">glScaled</a> and <b>glScalef</b> functions multiply the current matrix by a general scaling matrix.


## -parameters




### -param x

Scale factors along the <i>x</i> axis.


### -param y

Scale factors along the <i>y</i> axis.


### -param z

Scale factors along the <i>z</i> axis.


## -returns



This function does not return a value.




## -remarks



The <b>glScalef</b> function produces a general scaling along the <i>x</i>, <i>y</i>, and <i>z</i> axes. The three arguments indicate the desired scale factors along each of the three axes. The resulting matrix appears in the following image.

<img alt="" border="0" src="images/scale01.png"/>

The current matrix (see <a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>) is multiplied by this scale matrix, with the product replacing the current matrix. That is, if M is the current matrix and S is the scale matrix, then M is replaced with M • S.

If the matrix mode is either GL_MODELVIEW or GL_PROJECTION, all objects drawn after <b>glScalef</b> is called are scaled. Use <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a> to save and restore the unscaled coordinate system.

If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled (<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> with argument GL_NORMALIZE).

The following functions retrieve information related to <b>glScalef</b>:


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



<a href="https://msdn.microsoft.com/9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6">glRotated</a>



<a href="https://msdn.microsoft.com/8216a125-de8c-44e5-afb3-3d4e5ffc600d">glRotatef</a>



<a href="https://msdn.microsoft.com/7aa8dc2c-c353-48d3-88a9-389521bed7c9">glTranslate</a>
 

 

