---
UID: NF:gl.glTexEnvi
title: glTexEnvi function
author: windows-driver-content
description: The glTexEnvi function sets a texture environment parameter.
old-location: opengl\gltexenvi.htm
old-project: OpenGL
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glTexEnvi, glTexEnvi, glTexEnvi function [OpenGL], opengl.gltexenvi
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
-	glTexEnvi
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTexEnvi function


## -description


The <b>glTexEnvi</b> function sets a texture environment parameter.


## -parameters




### -param target

A texture environment. Must be GL_TEXTURE_ENV.


### -param pname

The symbolic name of a single-valued texture environment parameter. Must be GL_TEXTURE_ENV_MODE.


### -param param

A single symbolic constant, one of GL_MODULATE, GL_DECAL, GL_BLEND, or GL_REPLACE.


## -returns



This function does not return a value.




## -remarks



A texture environment specifies how texture values are interpreted when a fragment is textured. The <i>target</i> parameter must be GL_TEXTURE_ENV. The <i>pname</i> parameter  is GL_TEXTURE_ENV_MODE. Three texture functions are defined: GL_MODULATE, GL_DECAL, and GL_BLEND.

A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see <a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>) and produces an RGBA color for that fragment. The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen. <i>C</i> is a triple of color values (RGB) and <i>A</i> is the associated alpha value. RGBA values extracted from a texture image are in the range [0, 1]. The subscript <i>f</i> refers to the incoming fragment, the subscript <i>t</i> to the texture image, the subscript <i>c</i> to the texture environment color, and subscript <i>v</i> indicates a value produced by the texture function.

A texture image can have up to four components per texture element (see <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> and <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>). In a one-component image, Lt indicates that single component. A two-component image uses <i>L</i><i>ₜ</i>  and <i>A</i><i>ₜ</i> . A three-component image has only a color value, <i>C</i><i>ₜ</i> . A four-component image has both a color value <i>C</i><i>ₜ</i>  and an alpha value <i>A</i><i>ₜ</i> .

<table>
<tr>
<th>Number of components</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
<tr>
<td rowspan="2">1</td>
<td><i>C</i><i><sub>v</sub></i> = <i>L</i><i>ₜ</i> <i>C</i><i><sub>f</sub></i></td>
<td rowspan="2">undefined</td>
<td><i>C</i><i><sub>v</sub></i> = <i>(1</i> - <i>L</i><i>ₜ</i> <i>)C</i><i><sub>f</sub></i> + <i>L</i><i>ₜ</i> <i>C</i><i><sub>c</sub></i></td>
</tr>
<tr>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i></td>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i></td>
</tr>
<tr>
<td rowspan="2">2</td>
<td><i>C</i><i><sub>v</sub></i> = <i>L</i><i>ₜ</i> <i>C</i><i><sub>f</sub></i></td>
<td rowspan="2">undefined</td>
<td><i>C</i><i><sub>v</sub></i> = <i>(1</i> - <i>L</i><i>ₜ</i> <i>)C</i><i><sub>f</sub></i> + <i>L</i><i>ₜ</i> <i>C</i><i><sub>c</sub></i></td>
</tr>
<tr>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i></td>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i></td>
</tr>
<tr>
<td rowspan="2">3</td>
<td><i>C</i><i><sub>v</sub></i> = <i>C</i><i>ₜ</i> <i>C</i><i><sub>f</sub></i></td>
<td><i>C</i><i><sub>v</sub></i> = <i>C</i><i>ₜ</i></td>
<td rowspan="2">undefined</td>
</tr>
<tr>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i> </td>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i></td>
</tr>
<tr>
<td rowspan="2">4</td>
<td><i>C</i><i><sub>v</sub></i> = <i>C</i><i>ₜ</i> <i>C</i><i><sub>f</sub></i></td>
<td><i>C</i><i><sub>v</sub></i> = (1 - <i>A</i><i>ₜ</i> <i>)C</i><i><sub>f</sub></i> + <i>A</i><i>ₜ</i> <i>C</i><i>ₜ</i></td>
<td rowspan="2">undefined</td>
</tr>
<tr>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i>ₜ</i> <i>A</i><i><sub>f</sub></i> </td>
<td><i>A</i><i><sub>v</sub></i> = <i>A</i><i><sub>f</sub></i></td>
</tr>
</table>
 

GL_TEXTURE_ENV_MODE defaults to GL_MODULATE.

The following function retrieves information related to <b>glTexEnvi</b>:


<a href="https://msdn.microsoft.com/c1429cb9-4392-41ef-a978-a51db66445f2">glTexGetEnviv</a>





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

