---
UID: NF:gl.glTranslatef
title: glTranslatef function
author: windows-driver-content
description: The glTranslatef function multiplies the current matrix by a translation matrix.
old-location: opengl\gltranslatef.htm
old-project: OpenGL
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glTranslatef, glTranslatef, glTranslatef function [OpenGL], opengl.gltranslatef
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
-	glTranslatef
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTranslatef function


## -description


The <a href="https://msdn.microsoft.com/7aa8dc2c-c353-48d3-88a9-389521bed7c9">glTranslatef</a> function multiplies the current matrix by a translation matrix.


## -parameters




### -param x

The <i>x</i> coordinate of a translation vector.


### -param y

The <i>y</i> coordinate of a translation vector.


### -param z

The <i>z</i> coordinate of a translation vector.


## -returns



This function does not return a value.




## -remarks



The <b>glTranslatef</b> function produces the translation specified by (<i>x</i>, <i>y</i>, <i>z</i>). The translation vector is used to compute a 4x4 translation matrix:

<img alt="" border="0" src="images/trans01.png"/>
The current matrix (see <a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>) is multiplied by this translation matrix, with the product replacing the current matrix. That is, if M is the current matrix and T is the translation matrix, then M is replaced with M•T.

If the matrix mode is either GL_MODELVIEW or GL_PROJECTION, all objects drawn after <b>glTranslatef</b> is called are translated. Use <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <b>glPopMatrix</b> to save and restore the untranslated coordinate system.

The following functions retrieve information related to <a href="https://msdn.microsoft.com/7aa8dc2c-c353-48d3-88a9-389521bed7c9">glTranslated</a> and <b>glTranslatef</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE

<b>glGet</b> with argument GL_MODELVIEW_MATRIX

<b>glGet</b> with argument GL_PROJECTION_MATRIX

<b>glGet</b> with argument GL_TEXTURE_MATRIX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>



<a href="https://msdn.microsoft.com/f095df24-0773-4d72-8382-40986f72fc6b">glRotate</a>



<a href="https://msdn.microsoft.com/4c7e5598-534d-4b81-bb58-2e89d0dbfc77">glScale</a>
 

 

