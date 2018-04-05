---
UID: NF:gl.glLightModeli
title: glLightModeli function
author: windows-driver-content
description: The glLightModeli function sets lighting model parameters.
old-location: opengl\gllightmodeli.htm
old-project: OpenGL
ms.assetid: 49975166-b2b3-47f9-8305-aea2ba364546
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_LIGHT_MODEL_LOCAL_VIEWER, GL_LIGHT_MODEL_TWO_SIDE, gl/glLightModeli, glLightModeli, glLightModeli function [OpenGL], opengl.gllightmodeli
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
-	glLightModeli
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLightModeli function


## -description


The <a href="https://msdn.microsoft.com/d9f93fd9-6674-486f-a3fc-c10255dd37e7">glLightModeli</a> function sets lighting model parameters.


## -parameters




### -param pname

A single-valued lighting model parameter. The following values are accepted. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_LOCAL_VIEWER"></a><a id="gl_light_model_local_viewer"></a><dl>
<dt><b>GL_LIGHT_MODEL_LOCAL_VIEWER</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer value that specifies how specular reflection angles are computed. If <i>param</i> is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -<i>z</i> axis, regardless of the location of the vertex in eye coordinates. Otherwise, specular reflections are computed from the origin of the eye coordinate system. The default is 0. 


</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_TWO_SIDE"></a><a id="gl_light_model_two_side"></a><dl>
<dt><b>GL_LIGHT_MODEL_TWO_SIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>param</i> parameter is a single integer value that specifies whether one-sided or two-sided lighting calculations are done for polygons. It has no effect on the lighting calculations for points, lines, or bitmaps. If <i>param</i> is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation. Otherwise, two-sided lighting is specified. 

In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated. Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals. The default is 0.

</td>
</tr>
</table>
 


### -param param

The value to which <i>param</i> will be set.


## -returns



This function does not return a value.




## -remarks



The <b>glLightModeli</b> function sets lighting model parameter. The <i>pname</i> parameter names a parameter and <i>param</i> gives the new value.the value or values of individual light source parameters. 

In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source. Each light source contributes the sum of three terms: ambient, diffuse, and specular. 
		

<ul>
<li>The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</li>
<li>The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</li>
<li>The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</li>
</ul>
All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle. All dot products are replaced with zero if they evaluate to a negative value.

The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.

In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to <a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a> using GL_COLOR_INDEXES. Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.

The following functions retrieve information related to the <b>glLightModeli</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LIGHT_MODEL_LOCAL_VIEWER


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LIGHT_MODEL_TWO_SIDE


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_LIGHTING




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
 

 

