---
UID: NF:gl.glLoadIdentity
title: glLoadIdentity function
author: windows-driver-content
description: The glLoadIdentity function replaces the current matrix with the identity matrix.
old-location: opengl\glloadidentity.htm
old-project: OpenGL
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glLoadIdentity, gl/glLoadIdentity, glLoadIdentity, glLoadIdentity function [OpenGL], opengl.glloadidentity"
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
-	glLoadIdentity
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLoadIdentity function


## -description


The <b>glLoadIdentity</b> function replaces the current matrix with the identity matrix.


## -parameters






## -returns



This function does not return a value.




## -remarks



The <b>glLoadIdentity</b> function replaces the current matrix with the identity matrix. It is semantically equivalent to calling <a href="https://msdn.microsoft.com/a55575a8-fd1d-4f5b-a5c7-c158c1ef0fee">glLoadMatrix</a> with the following identity matrix.

<img alt="" border="0" src="images/load01.png"/>
However, in some cases, it is more efficient.

The following functions retrieve information related to <b>glLoadIdentity</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE

<b>glGet</b> with argument GL_MODELVIEW_MATRIX

<b>glGet</b> with argument GL_PROJECTION_MATRIX

<b>glGet</b> with argument GL_TEXTURE_MATRIX




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a55575a8-fd1d-4f5b-a5c7-c158c1ef0fee">glLoadMatrix</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>
 

 

