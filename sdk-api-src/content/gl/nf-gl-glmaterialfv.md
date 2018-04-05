---
UID: NF:gl.glMaterialfv
title: glMaterialfv function
author: windows-driver-content
description: The glMaterialfv function specifies material parameters for the lighting model.
old-location: opengl\glmaterialfv.htm
old-project: OpenGL
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_AMBIENT, GL_AMBIENT_AND_DIFFUSE, GL_COLOR_INDEXES, GL_DIFFUSE, GL_EMISSION, GL_SHININESS, GL_SPECULAR, gl/glMaterialfv, glMaterialfv, glMaterialfv function [OpenGL], opengl.glmaterialfv
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
-	glMaterialfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glMaterialfv function


## -description


The <b>glMaterialfv</b> function specifies material parameters for the lighting model.


## -parameters




### -param face

The face or faces that are being updated. Must be one of the following: GL_FRONT, GL_BACK, or GL_FRONT and GL_BACK.


### -param pname

The material parameter of the face or faces being updated. The parameters that can be specified using <b>glMaterialfv</b>, and their interpretations by the lighting equation, are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_AMBIENT"></a><a id="gl_ambient"></a><dl>
<dt><b>GL_AMBIENT</b></dt>
</dl>
</td>
<td width="60%">
The params parameter contains four floating-point values that specify the ambient RGBA reflectance of the material. Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. Floating-point values are mapped directly. Neither integer nor floating-point values are clamped. The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0). 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DIFFUSE"></a><a id="gl_diffuse"></a><dl>
<dt><b>GL_DIFFUSE</b></dt>
</dl>
</td>
<td width="60%">
The params parameter contains four floating-point values that specify the diffuse RGBA reflectance of the material. Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. Floating-point values are mapped directly. Neither integer nor floating-point values are clamped. The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0). 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPECULAR"></a><a id="gl_specular"></a><dl>
<dt><b>GL_SPECULAR</b></dt>
</dl>
</td>
<td width="60%">
The params parameter contains four floating-point values that specify the specular RGBA reflectance of the material. Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. Floating-point values are mapped directly. Neither integer nor floating-point values are clamped. The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0). 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EMISSION"></a><a id="gl_emission"></a><dl>
<dt><b>GL_EMISSION</b></dt>
</dl>
</td>
<td width="60%">
The params parameter contains four floating-point values that specify the RGBA emitted light intensity of the material. Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. Floating-point values are mapped directly. Neither integer nor floating-point values are clamped. The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0). 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SHININESS"></a><a id="gl_shininess"></a><dl>
<dt><b>GL_SHININESS</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer value that specifies the RGBA specular exponent of the material. Integer values are mapped directly. Only values in the range [0, 128] are accepted. The default specular exponent for both front-facing and back-facing materials is 0. 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AMBIENT_AND_DIFFUSE"></a><a id="gl_ambient_and_diffuse"></a><dl>
<dt><b>GL_AMBIENT_AND_DIFFUSE</b></dt>
</dl>
</td>
<td width="60%">
Equivalent to calling <a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a> twice with the same parameter values, once with GL_AMBIENT and once with GL_DIFFUSE. 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_INDEXES"></a><a id="gl_color_indexes"></a><dl>
<dt><b>GL_COLOR_INDEXES</b></dt>
</dl>
</td>
<td width="60%">
The params parameter contains three floating-point values specifying the color indexes for ambient, diffuse, and specular lighting. These three values, and GL_SHININESS, are the only material values used by the color-index mode lighting equation. Refer to <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a> for a discussion of color-index lighting.

</td>
</tr>
</table>
 


### -param params

The value to which parameter GL_SHININESS will be set.


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/c6d183c4-2d1f-4fb9-b24f-c132ebfc708d">glMaterialfv</a> function assigns values to material parameters. There are two matched sets of material parameters. One, the <i>front-facing</i> set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled). The other set, <i>back-facing</i>, is used to shade back-facing polygons only when two-sided lighting is enabled. Refer to <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a> for details concerning one-sided and two-sided lighting calculations.

The <a href="https://msdn.microsoft.com/c6d183c4-2d1f-4fb9-b24f-c132ebfc708d">glMaterialfv</a> function takes three arguments. The first, <i>face</i>, specifies whether the GL_FRONT materials, the GL_BACK materials, or both GL_FRONT_AND_BACK materials will be modified. The second, <i>pname</i>, specifies which of several parameters in one or both sets will be modified. The third, <i>param</i>, specifies what value will be assigned to the specified parameter.

Material parameters are used in the lighting equation that is optionally applied to each vertex. The equation is discussed in <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

The material parameters can be updated at any time. In particular, <a href="https://msdn.microsoft.com/c6d183c4-2d1f-4fb9-b24f-c132ebfc708d">glMaterialfv</a> can be called between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>. If only a single material parameter is to be changed per vertex, however, <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a> is preferred over <b>glMaterialfv</b>.

The following function retrieves information related to <a href="https://msdn.microsoft.com/c6d183c4-2d1f-4fb9-b24f-c132ebfc708d">glMaterialfv</a>:


<a href="https://msdn.microsoft.com/79409f4e-1e39-4fca-adc8-d48253853ce3">glGetMaterial</a>





## -see-also




<a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>
 

 

