---
UID: NF:gl.glPopMatrix
title: glPopMatrix function
author: windows-driver-content
description: The glPushMatrix and glPopMatrix functions push and pop the current matrix stack.
old-location: opengl\glpopmatrix.htm
old-project: OpenGL
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPopMatrix, glPopMatrix, glPopMatrix function [OpenGL], opengl.glpopmatrix
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
-	glPopMatrix
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPopMatrix function


## -description


The <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <b>glPopMatrix</b> functions push and pop the current matrix stack.


## -parameters






## -returns



This function does not return a value.




## -remarks



There is a stack of matrices for each of the matrix modes. In GL_MODELVIEW mode, the stack depth is at least 32. In the other two modes, GL_PROJECTION and GL_TEXTURE, the depth is at least 2. The current matrix in any mode is the matrix on the top of the stack for that mode.

The <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> function pushes the current matrix stack down by one, duplicating the current matrix. That is, after a <b>glPushMatrix</b> call, the matrix on the top of the stack is identical to the one below it. The <b>glPopMatrix</b> function pops the current matrix stack, replacing the current matrix with the one below it on the stack. Initially, each of the stacks contains one matrix, an identity matrix.

The following functions retrieve information related to <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a> and <b>glPopMatrix</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE

<b>glGet</b> with argument GL_MODELVIEW_MATRIX

<b>glGet</b> with argument GL_PROJECTION_MATRIX

<b>glGet</b> with argument GL_TEXTURE_MATRIX

<b>glGet</b> with argument GL_MODELVIEW_STACK_DEPTH

<b>glGet</b> with argument GL_PROJECTION_STACK_DEPTH

<b>glGet</b> with argument GL_TEXTURE_STACK_DEPTH

<b>glGet</b> with argument GL_MAX_MODELVIEW_STACK_DEPTH

<b>glGet</b> with argument GL_MAX_PROJECTION_STACK_DEPTH

<b>glGet</b> with argument GL_MAX_TEXTURE_STACK_DEPTH




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3">glFrustum</a>



<a href="https://msdn.microsoft.com/59273aa9-4db3-4c8c-8364-f54c03d2f97a">glLoadIdentity</a>



<a href="https://msdn.microsoft.com/a55575a8-fd1d-4f5b-a5c7-c158c1ef0fee">glLoadMatrix</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/0d076023-03e3-4ced-8e0a-ebff903ffdec">glMultMatrix</a>



<a href="https://msdn.microsoft.com/5c70819f-e9b6-49e2-add5-9f6e6aba26ee">glOrtho</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>



<a href="https://msdn.microsoft.com/f095df24-0773-4d72-8382-40986f72fc6b">glRotate</a>



<a href="https://msdn.microsoft.com/4c7e5598-534d-4b81-bb58-2e89d0dbfc77">glScale</a>



<a href="https://msdn.microsoft.com/7aa8dc2c-c353-48d3-88a9-389521bed7c9">glTranslate</a>



<a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>
 

 

