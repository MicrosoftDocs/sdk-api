---
UID: NF:gl.glLightModelfv
title: glLightModelfv function
author: windows-driver-content
description: The glLightModelfv function sets lighting model parameters.
old-location: opengl\gllightmodelfv.htm
old-project: OpenGL
ms.assetid: a62bcf3b-1769-48a3-8121-8f2b41266183
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_LIGHT_MODEL_AMBIENT, GL_LIGHT_MODEL_LOCAL_VIEWER, GL_LIGHT_MODEL_TWO_SIDE, gl/glLightModelfv, glLightModelfv, glLightModelfv function [OpenGL], opengl.gllightmodelfv
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
-	glLightModelfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLightModelfv function


## -description


The <a href="https://msdn.microsoft.com/0a9feb00-f64a-43fc-b9ca-8a97fdaf4de9">glLightModelfv</a> function sets lighting model parameters.


## -parameters




### -param pname

A lighting model parameter. The following values are accepted. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_AMBIENT"></a><a id="gl_light_model_ambient"></a><dl>
<dt><b>GL_LIGHT_MODEL_AMBIENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter contains four floating-point values that specify the ambient RGBA intensity of the entire scene. Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. Floating-point values are mapped directly. Neither integer nor floating-point values are clamped. The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0). 

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_LOCAL_VIEWER"></a><a id="gl_light_model_local_viewer"></a><dl>
<dt><b>GL_LIGHT_MODEL_LOCAL_VIEWER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single floating-point value that specifies how specular reflection angles are computed. If <i>param</i> is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -<i>z</i> axis, regardless of the location of the vertex in eye coordinates. Otherwise, specular reflections are computed from the origin of the eye coordinate system. The default is 0. 


</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_TWO_SIDE"></a><a id="gl_light_model_two_side"></a><dl>
<dt><b>GL_LIGHT_MODEL_TWO_SIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons. It has no effect on the lighting calculations for points, lines, or bitmaps. If <i>param</i> is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation. Otherwise, two-sided lighting is specified. 

In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated. Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals. The default is 0.

</td>
</tr>
</table>
 


### -param params

A pointer to the value or values to which <i>params</i> will be set.


## -returns



This function does not return a value.




## -remarks



The <b>glLightModelfv</b> function sets lighting model parameter. The <i>pname</i> parameter names a parameter and <i>param</i> gives the new value.the value or values of individual light source parameters. 

In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source. Each light source contributes the sum of three terms: ambient, diffuse, and specular. 
		

<ul>
<li>The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</li>
<li>The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</li>
<li>The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</li>
</ul>
All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle. All dot products are replaced with zero if they evaluate to a negative value.

The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.

In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to <a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a> using GL_COLOR_INDEXES. Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.

The following functions retrieve information related to the <b>glLightModelfv</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LIGHT_MODEL_LOCAL_VIEWER


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LIGHT_MODEL_TWO_SIDE


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_LIGHTING




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
 

 

