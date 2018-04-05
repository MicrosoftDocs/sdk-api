---
UID: NF:gl.glMateriali
title: glMateriali function
author: windows-driver-content
description: TheglMateriali function specifies material parameters for the lighting model.
old-location: opengl\glmateriali.htm
old-project: OpenGL
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_SHININESS, gl/glMateriali, glMateriali, glMateriali function [OpenGL], opengl.glmateriali
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
-	glMateriali
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glMateriali function


## -description


The<b>glMateriali</b> function specifies material parameters for the lighting model.


## -parameters




### -param face

The face or faces that are being updated. Must be one of the following: GL_FRONT, GL_BACK, or GL_FRONT and GL_BACK.


### -param pname

The single-valued material parameter of the face or faces being updated. Must be GL_SHININESS.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_SHININESS"></a><a id="gl_shininess"></a><dl>
<dt><b>GL_SHININESS</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer that specifies the RGBA specular exponent of the material. Integer values are mapped directly. Only values in the range [0, 128] are accepted. The default specular exponent for both front-facing and back-facing materials is 0. 

</td>
</tr>
</table>
 


### -param param

The value to which parameter GL_SHININESS will be set.


## -returns



This function does not return a value.




## -remarks



The <b>glMateriali</b> function assigns values to material parameters. There are two matched sets of material parameters. One, the <i>front-facing</i> set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled). The other set, <i>back-facing</i>, is used to shade back-facing polygons only when two-sided lighting is enabled. Refer to <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a> for details concerning one-sided and two-sided lighting calculations.

The <b>glMateriali</b> function takes three arguments. The first, <i>face</i>, specifies whether the GL_FRONT materials, the GL_BACK materials, or both GL_FRONT_AND_BACK materials will be modified. The second, <i>pname</i>, specifies which of several parameters in one or both sets will be modified. The third, <i>param</i>, specifies what value will be assigned to the specified parameter.

Material parameters are used in the lighting equation that is optionally applied to each vertex. The equation is discussed in <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

The material parameters can be updated at any time. In particular, <b>glMateriali</b> can be called between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>. If only a single material parameter is to be changed per vertex, however, <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a> is preferred over <b>glMateriali</b>.

The following function retrieves information related to <b>glMateriali</b>:


<a href="https://msdn.microsoft.com/79409f4e-1e39-4fca-adc8-d48253853ce3">glGetMaterial</a>





## -see-also




<a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>
 

 

