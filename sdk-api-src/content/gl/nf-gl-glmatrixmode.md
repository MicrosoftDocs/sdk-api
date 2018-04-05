---
UID: NF:gl.glMatrixMode
title: glMatrixMode function
author: windows-driver-content
description: The glMatrixMode function specifies which matrix is the current matrix.
old-location: opengl\glmatrixmode.htm
old-project: OpenGL
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_MODELVIEW, GL_PROJECTION, GL_TEXTURE, _ogl_glMatrixMode, gl/glMatrixMode, glMatrixMode, glMatrixMode function [OpenGL], opengl.glmatrixmode
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
-	glMatrixMode
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glMatrixMode function


## -description


The <b>glMatrixMode</b> function specifies which matrix is the current matrix.


## -parameters




### -param mode

The matrix stack that is the target for subsequent matrix operations. The <i>mode</i> parameter can assume one of three values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_MODELVIEW"></a><a id="gl_modelview"></a><dl>
<dt><b>GL_MODELVIEW</b></dt>
</dl>
</td>
<td width="60%">
Applies subsequent matrix operations to the modelview matrix stack.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PROJECTION"></a><a id="gl_projection"></a><dl>
<dt><b>GL_PROJECTION</b></dt>
</dl>
</td>
<td width="60%">
Applies subsequent matrix operations to the projection matrix stack.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE"></a><a id="gl_texture"></a><dl>
<dt><b>GL_TEXTURE</b></dt>
</dl>
</td>
<td width="60%">
Applies subsequent matrix operations to the texture matrix stack.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glMatrixMode</b> function sets the current matrix mode.

The following function retrieves information related to <b>glMatrixMode</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a55575a8-fd1d-4f5b-a5c7-c158c1ef0fee">glLoadMatrix</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>
 

 

