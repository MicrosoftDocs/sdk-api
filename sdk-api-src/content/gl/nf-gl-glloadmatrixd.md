---
UID: NF:gl.glLoadMatrixd
title: glLoadMatrixd function
author: windows-driver-content
description: The glLoadMatrixd and glLoadMatrixf functions replace the current matrix with an arbitrary matrix.
old-location: opengl\glloadmatrixd.htm
old-project: OpenGL
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glLoadMatrixd, glLoadMatrixd, glLoadMatrixd function [OpenGL], opengl.glloadmatrixd
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
-	glLoadMatrixd
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLoadMatrixd function


## -description


The <b>glLoadMatrixd</b> and <a href="https://msdn.microsoft.com/6e1337b0-d1e7-4002-a561-d959d7f70942">glLoadMatrixf</a> functions replace the current matrix with an arbitrary matrix.


## -parameters




### -param m

A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.


## -returns



This function does not return a value.




## -remarks



The <b>glLoadMatrix</b> function replaces the current matrix with the one specified in <i>m</i>. The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see <a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>).

The <i>m</i> parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order. That is, the matrix is stored as shown in the following image.

<img alt="" border="0" src="images/load02.png"/>
The following functions retrieve information related to <b>glLoadMatrix</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE

<b>glGet</b> with argument GL_MODELVIEW_MATRIX

<b>glGet</b> with argument GL_PROJECTION_MATRIX

<b>glGet</b> with argument GL_TEXTURE_MATRIX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/59273aa9-4db3-4c8c-8364-f54c03d2f97a">glLoadIdentity</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>
 

 

