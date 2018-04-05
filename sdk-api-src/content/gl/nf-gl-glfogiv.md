---
UID: NF:gl.glFogiv
title: glFogiv function
author: windows-driver-content
description: The glFogfv function specifies fog parameters.
old-location: opengl\glfogiv.htm
old-project: OpenGL
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_FOG_COLOR, GL_FOG_DENSITY, GL_FOG_END, GL_FOG_INDEX, GL_FOG_MODE, GL_FOG_START, gl/glFogiv, glFogiv, glFogiv function [OpenGL], opengl.glfogiv
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
-	glFogiv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glFogiv function


## -description


The <b>glFogfv</b> function specifies fog parameters.


## -parameters




### -param pname

Specifies a fog parameter.

Accepts one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_MODE"></a><a id="gl_fog_mode"></a><dl>
<dt><b>GL_FOG_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, <i>f</i>. Three symbolic constants are accepted: GL_LINEAR, GL_EXP, and GL_EXP2. The equations corresponding to these symbolic constants are defined in the following Remarks section. The default fog mode is GL_EXP.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_DENSITY"></a><a id="gl_fog_density"></a><dl>
<dt><b>GL_FOG_DENSITY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single integer value that specifies <i>density</i>, the fog density used in both exponential fog equations. Only nonnegative densities are accepted. The default fog density is 1.0.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_START"></a><a id="gl_fog_start"></a><dl>
<dt><b>GL_FOG_START</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single integer value that specifies <i>start</i>, the near distance used in the linear fog equation. The default near distance is 0.0.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_END"></a><a id="gl_fog_end"></a><dl>
<dt><b>GL_FOG_END</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single integer value that specifies <i>end</i>, the far distance used in the linear fog equation. The default far distance is 1.0.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_INDEX"></a><a id="gl_fog_index"></a><dl>
<dt><b>GL_FOG_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter is a single integer value that specifies <i>i</i><sub>f</sub> , the fog color index. The default fog index is 0.0.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_COLOR"></a><a id="gl_fog_color"></a><dl>
<dt><b>GL_FOG_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter contains four integer or floating-point values that specify <i>C</i><sub>f</sub> , the fog color. Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. Floating-point values are mapped directly. After conversion, all color components are clamped to the range [0,1]. The default fog color is (0,0,0,0).

</td>
</tr>
</table>
 


### -param params

Specifies the value or values to be assigned to <i>pname</i>. GL_FOG_COLOR requires an array of four values. All other parameters accept an array containing only a single value.


## -returns



This function does not return a value.




## -remarks



You enable and disable fog with <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>, using the argument GL_FOG. While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.

The <b>glFogiv</b> function assigns the value or values in <i>params</i> to the fog parameter specified by <i>pname</i>.

Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor <i>f</i>. Factor <i>f</i> is computed in one of three ways, depending on the fog mode. Let <i>z</i> be the distance in eye coordinates from the origin to the fragment being fogged. The equation for GL_LINEAR fog is:

<img alt="" border="0" src="images/fog01.png"/>
The equation for GL_EXP fog is:

<img alt="" border="0" src="images/fog02.png"/>
The equation for GL_EXP2 fog is:

<img alt="" border="0" src="images/fog03.png"/>
Regardless of the fog mode, <i>f</i> is clamped to the range [0,1] after it is computed. Then, if OpenGL is in RGBA color mode, the fragment's color <i>C</i><sub>r</sub> is replaced by

<img alt="" border="0" src="images/fog04.png"/>
In color-index mode, the fragment's color index <i>i</i><sub>r</sub> is replaced by

<img alt="" border="0" src="images/fog05.png"/>
The following functions retrieve information related to the <b>glFog</b> functions:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_FOG_COLOR

<b>glGet</b> with argument GL_FOG_INDEX

<b>glGet</b> with argument GL_FOG_DENSITY

<b>glGet</b> with argument GL_FOG_START

<b>glGet</b> with argument GL_FOG_END

<b>glGet</b> with argument GL_FOG_MODE


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_FOG




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

