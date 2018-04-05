---
UID: NF:gl.glGetMaterialfv
title: glGetMaterialfv function
author: windows-driver-content
description: The glGetMaterialfv and glGetMaterialiv functions return material parameters.
old-location: opengl\glgetmaterialfv.htm
old-project: OpenGL
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_AMBIENT, GL_COLOR_INDEXES, GL_DIFFUSE, GL_EMISSION, GL_SHININESS, GL_SPECULAR, gl/glGetMaterialfv, glGetMaterialfv, glGetMaterialfv function [OpenGL], opengl.glgetmaterialfv
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
-	glGetMaterialfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetMaterialfv function


## -description


The <b>glGetMaterialfv</b> and <a href="https://msdn.microsoft.com/459cbe8a-a51a-496e-bdd1-89b8cf486a46">glGetMaterialiv</a> functions return material parameters.


## -parameters




### -param face

Specifies which of the two materials is being queried. GL_FRONT or GL_BACK are accepted, representing the front and back materials, respectively.


### -param pname

The material parameter to return. The following values are accepted.

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
The <i>params</i> parameter returns four integer or floating-point values representing the ambient reflectance of the material. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DIFFUSE"></a><a id="gl_diffuse"></a><dl>
<dt><b>GL_DIFFUSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values representing the diffuse reflectance of the material. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SPECULAR"></a><a id="gl_specular"></a><dl>
<dt><b>GL_SPECULAR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values representing the specular reflectance of the material. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EMISSION"></a><a id="gl_emission"></a><dl>
<dt><b>GL_EMISSION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values representing the emitted light intensity of the material. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value. If the internal value is outside the range [-1,1], the corresponding integer return value is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SHININESS"></a><a id="gl_shininess"></a><dl>
<dt><b>GL_SHININESS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one integer or floating-point value representing the specular exponent of the material. Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_INDEXES"></a><a id="gl_color_indexes"></a><dl>
<dt><b>GL_COLOR_INDEXES</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material. Use these indexes only for color-index lighting. (The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.

</td>
</tr>
</table>
 


### -param params

Returns the requested data.


## -returns



This function does not return a value.




## -remarks



The <b>glGetMaterial</b> function returns in <i>params</i> the value or values of parameter <i>pname</i> of material <i>face</i>.

If an error is generated, no change is made to the contents of <i>params</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
 

 

