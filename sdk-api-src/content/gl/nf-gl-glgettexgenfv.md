---
UID: NF:gl.glGetTexGenfv
title: glGetTexGenfv function
author: windows-driver-content
description: The glGetTexGendv, glGetTexGenfv, and glGetTexGeniv functions return texture coordinate generation parameters.
old-location: opengl\glgettexgenfv.htm
old-project: OpenGL
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_EYE_PLANE, GL_OBJECT_PLANE, GL_TEXTURE_GEN_MODE, gl/glGetTexGenfv, glGetTexGenfv, glGetTexGenfv function [OpenGL], opengl.glgettexgenfv
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
-	glGetTexGenfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetTexGenfv function


## -description


The <a href="https://msdn.microsoft.com/bce26bde-071b-476e-9e33-c43a8c997cdd">glGetTexGendv</a>, <b>glGetTexGenfv</b>, and <a href="https://msdn.microsoft.com/62c481d1-4862-43bb-9319-5a282c4e47d3">glGetTexGeniv</a> functions return texture coordinate generation parameters.


## -parameters




### -param coord

A texture coordinate. Must be GL_S, GL_T, GL_R, or GL_Q.


### -param pname

The symbolic name of the value(s) to be returned. Must be either GL_TEXTURE_GEN_MODE or the name of one of the texture generation plane equations: GL_OBJECT_PLANE or GL_EYE_PLANE. These values are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_MODE"></a><a id="gl_texture_gen_mode"></a><dl>
<dt><b>GL_TEXTURE_GEN_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns the single-valued texture generation function, a symbolic constant.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_OBJECT_PLANE"></a><a id="gl_object_plane"></a><dl>
<dt><b>GL_OBJECT_PLANE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns the four plane equation coefficients that specify object linear-coordinate generation. Integer values, when requested, are mapped directly from the internal floating-point representation.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EYE_PLANE"></a><a id="gl_eye_plane"></a><dl>
<dt><b>GL_EYE_PLANE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns the four plane equation coefficients that specify eye linear-coordinate generation. Integer values, when requested, are mapped directly from the internal floating-point representation. The returned values are those maintained in eye coordinates. They are not equal to the values specified using <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>, unless the modelview matrix was identified at the time <b>glTexGen</b> was called.

</td>
</tr>
</table>
 


### -param params

Returns the requested data.


## -returns



This function does not return a value.




## -remarks



The <b>glGetTexGen</b> function returns in <i>params</i> selected parameters of a texture-coordinate generation function that you specified with <b>glTexGen</b>. The <i>coord</i> parameter names one of the (<i>s</i>, <i>t</i>, <i>r</i>, <i>q</i>) texture coordinates, using the symbolic constant GL_S, GL_T, GL_R, or GL_Q.

If an error is generated, no change is made to the contents of <i>params</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>
 

 

