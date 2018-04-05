---
UID: NF:gl.glLighti
title: glLighti function
author: windows-driver-content
description: The glLighti function returns light source parameter values.
old-location: opengl\gllighti.htm
old-project: OpenGL
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_CONSTANT_ATTENUATION, GL_LINEAR_ATTENUATION, GL_QUADRATIC_ATTENUATION, GL_SPOT_CUTOFF, GL_SPOT_EXPONENT, gl/glLighti, glLighti, glLighti function [OpenGL], opengl.gllighti
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
-	glLighti
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLighti function


## -description


The <b>glLighti</b> function returns light source parameter values.


## -parameters




### -param light

The identifier of a light. The number of possible lights depends on the implementation, but at least eight lights are supported. They are identified by symbolic names of the form GL_LIGHT<i>i</i> where <i>i</i> is a value: 0 to GL_MAX_LIGHTS - 1.


### -param pname

A single-valued light source parameter for <i>light</i>. The following symbolic names are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_SPOT_EXPONENT"></a><a id="gl_spot_exponent"></a><dl>
<dt><b>GL_SPOT_EXPONENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer value that specifies the intensity distribution of the light. Integer and floating-point values are mapped directly. Only values in the range [0, 128] are accepted. 

Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent. Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle. The default spot exponent is 0, resulting in uniform light distribution.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPOT_CUTOFF"></a><a id="gl_spot_cutoff"></a><dl>
<dt><b>GL_SPOT_CUTOFF</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer value that specifies the maximum spread angle of a light source. Integer and floating-point values are mapped directly. Only values in the range [0, 90], and the special value 180, are accepted. 

If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked. Otherwise, its intensity is controlled by the spot exponent and the attenuation factors. The default spot cutoff is 180, resulting in uniform light distribution.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></a><a id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></a><dl>
<dt><b>GL_CONSTANT_ATTENUATION, GL_LINEAR_ATTENUATION, GL_QUADRATIC_ATTENUATION</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer value that specifies one of the three light attenuation factors. Integer and floating-point values are mapped directly. Only nonnegative values are accepted. 

If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance. The default attenuation factors are (1,0,0), resulting in no attenuation.

</td>
</tr>
</table>
 


### -param param

Specifies the value that parameter <i>pname</i> of light source <i>light</i> will be set to.


## -returns



This function does not return a value.




## -remarks



The <b>glLighti</b> function sets the value or values of individual light source parameters. The <i>light</i> parameter names the light and is a symbolic name of the form GL_LIGHT<i>i</i>, where 0 ≤ <i>i</i> &lt; GL_MAX_LIGHTS. 

The <i>pname</i> parameter specifies one of the light source parameters, again by symbolic name. The <i>param</i> parameter is either a single value or a pointer to an array that contains the new values.

Lighting calculation is enabled and disabled using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> with argument GL_LIGHTING. When lighting is enabled, light sources that are enabled contribute to the lighting calculation. Light source <i>i</i> is enabled and disabled using <b>glEnable</b> and <b>glDisable</b> with argument GL_LIGHT<i>i</i>.



It is always the case that GL_LIGHT<i>i</i> = GL_LIGHT0 + <i>i</i>.

The following functions retrieve information related to the <b>glLighti</b> function:


<a href="https://msdn.microsoft.com/a2d41afd-78d9-4c59-92d5-3334d14a42f3">glGetLight</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_LIGHTING




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
 

 

