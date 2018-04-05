---
UID: NF:gl.glGetLightfv
title: glGetLightfv function
author: windows-driver-content
description: The glGetLightfv and glGetLightiv functions return light source parameter values.
old-location: opengl\glgetlightfv.htm
old-project: OpenGL
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_AMBIENT, GL_CONSTANT_ATTENUATION, GL_DIFFUSE, GL_LINEAR_ATTENUATION, GL_POSITION, GL_QUADRATIC_ATTENUATION, GL_SPECULAR, GL_SPOT_CUTOFF, GL_SPOT_DIRECTION, GL_SPOT_EXPONENT, gl/glGetLightfv, glGetLightfv, glGetLightfv function [OpenGL], opengl.glgetlightfv
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
-	glGetLightfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetLightfv function


## -description


The <b>glGetLightfv</b> and <a href="https://msdn.microsoft.com/be4316ca-dc49-4bfa-929a-fa25f5057fde">glGetLightiv</a> functions return light source parameter values.


## -parameters




### -param light

A light source. The number of possible lights depends on the implementation, but at least eight lights are supported. They are identified by symbolic names of the form GL_LIGHT <i>i</i> where 0 ≤ <i>i</i> &lt; GL_MAX_LIGHTS.


### -param pname

A light source parameter for <i>light</i>. The following symbolic names are accepted.

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
The <i>params</i> parameter returns four integer or floating-point values representing the ambient intensity of the light source. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DIFFUSE"></a><a id="gl_diffuse"></a><dl>
<dt><b>GL_DIFFUSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values representing the diffuse intensity of the light source. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPECULAR"></a><a id="gl_specular"></a><dl>
<dt><b>GL_SPECULAR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values representing the specular intensity of the light source. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POSITION"></a><a id="gl_position"></a><dl>
<dt><b>GL_POSITION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values representing the position of the light source. Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer value. The returned values are those maintained in eye coordinates. They will not be equal to the values specified using <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>, unless the modelview matrix was identified at the time <b>glLight</b> was called.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPOT_DIRECTION"></a><a id="gl_spot_direction"></a><dl>
<dt><b>GL_SPOT_DIRECTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns three integer or floating-point values representing the direction of the light source. Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer value. The returned values are those maintained in eye coordinates. They will not be equal to the values specified using <b>glLight</b>, unless the modelview matrix was identified at the time <b>glLight</b> was called. Although spot direction is normalized before being used in the lighting equation, the returned values are the transformed versions of the specified values prior to normalization.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPOT_EXPONENT"></a><a id="gl_spot_exponent"></a><dl>
<dt><b>GL_SPOT_EXPONENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single integer or floating-point value representing the spot exponent of the light. An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPOT_CUTOFF"></a><a id="gl_spot_cutoff"></a><dl>
<dt><b>GL_SPOT_CUTOFF</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single integer or floating-point value representing the spot cutoff angle of the light. An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CONSTANT_ATTENUATION"></a><a id="gl_constant_attenuation"></a><dl>
<dt><b>GL_CONSTANT_ATTENUATION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single integer or floating-point value representing the constant (not distance-related) attenuation of the light. An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINEAR_ATTENUATION"></a><a id="gl_linear_attenuation"></a><dl>
<dt><b>GL_LINEAR_ATTENUATION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single integer or floating-point value representing the linear attenuation of the light. An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_QUADRATIC_ATTENUATION"></a><a id="gl_quadratic_attenuation"></a><dl>
<dt><b>GL_QUADRATIC_ATTENUATION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single integer or floating-point value representing the quadratic attenuation of the light. An integer value, when requested, is computed by rounding the internal floating-point representation to the nearest integer.

</td>
</tr>
</table>
 


### -param params

Returns the requested data.


## -returns



This function does not return a value.




## -remarks



The <b>glGetLight</b> function returns in <i>params</i> the value or values of a light source parameter. The <i>light</i> parameter names the light and is a symbolic name of the form GL_LIGHT<i>i</i> for 0 ≤ <i>i</i> &lt; GL_MAX_LIGHTS, where GL_MAX_LIGHTS is an implementation-dependent constant that is greater than or equal to eight. The <i>pname</i> parameter specifies one of ten light source parameters, again by symbolic name.

It is always the case that GL_LIGHT<i>i</i> = GL_LIGHT0 + <i>i</i>.

If an error is generated, no change is made to the contents of <i>params</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>
 

 

