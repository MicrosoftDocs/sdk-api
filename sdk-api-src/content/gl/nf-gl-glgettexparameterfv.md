---
UID: NF:gl.glGetTexParameterfv
title: glGetTexParameterfv function
author: windows-driver-content
description: The glGetTexParameterfv and glGetTexParameteriv functions return texture parameter values.
old-location: opengl\glgettexparameterfv.htm
old-project: OpenGL
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_TEXTURE_BORDER_COLOR, GL_TEXTURE_MAG_FILTER, GL_TEXTURE_MIN_FILTER, GL_TEXTURE_PRIORITY, GL_TEXTURE_RESIDENT, GL_TEXTURE_WRAP_S, GL_TEXTURE_WRAP_T, gl/glGetTexParameterfv, glGetTexParameterfv, glGetTexParameterfv function [OpenGL], opengl.glgettexparameterfv
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
-	glGetTexParameterfv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetTexParameterfv function


## -description


The <b>glGetTexParameterfv</b> and <a href="https://msdn.microsoft.com/b89d10f1-5e30-4d25-8953-fbd59781fdac">glGetTexParameteriv</a> functions return texture parameter values.


## -parameters




### -param target

The symbolic name of the target texture. GL_TEXTURE_1D and GL_TEXTURE_2D are accepted.


### -param pname

The symbolic name of a texture parameter. The following values are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_MAG_FILTER"></a><a id="gl_texture_mag_filter"></a><dl>
<dt><b>GL_TEXTURE_MAG_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Returns the single-valued texture magnification filter, a symbolic constant.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_MIN_FILTER"></a><a id="gl_texture_min_filter"></a><dl>
<dt><b>GL_TEXTURE_MIN_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Returns the single-valued texture minification filter, a symbolic constant.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_WRAP_S"></a><a id="gl_texture_wrap_s"></a><dl>
<dt><b>GL_TEXTURE_WRAP_S</b></dt>
</dl>
</td>
<td width="60%">
Returns the single-valued wrapping function for texture coordinate <i>s</i>, a symbolic constant.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_WRAP_T"></a><a id="gl_texture_wrap_t"></a><dl>
<dt><b>GL_TEXTURE_WRAP_T</b></dt>
</dl>
</td>
<td width="60%">
Returns the single-valued wrapping function for texture coordinate <i>t</i>, a symbolic constant.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_BORDER_COLOR"></a><a id="gl_texture_border_color"></a><dl>
<dt><b>GL_TEXTURE_BORDER_COLOR</b></dt>
</dl>
</td>
<td width="60%">
Returns four integer or floating-point numbers that comprise the RGBA color of the texture border. Floating-point values are returned in the range [0,1]. Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_PRIORITY"></a><a id="gl_texture_priority"></a><dl>
<dt><b>GL_TEXTURE_PRIORITY</b></dt>
</dl>
</td>
<td width="60%">
Returns the residence priority of the target texture (or the named texture bound to it). The initial value is 1. See <a href="https://msdn.microsoft.com/09018c86-c667-4e43-a95a-51a8077aed33">glPrioritizeTextures</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_RESIDENT"></a><a id="gl_texture_resident"></a><dl>
<dt><b>GL_TEXTURE_RESIDENT</b></dt>
</dl>
</td>
<td width="60%">
Returns the residence status of the target texture. If the value returned in params is GL_TRUE, the texture is resident in texture memory. See <a href="https://msdn.microsoft.com/55d068a8-d366-4fee-85d5-49373b8c5e02">glAreTexturesResident</a>.

</td>
</tr>
</table>
 


### -param params

Returns the texture parameters.


## -returns



This function does not return a value.




## -remarks



The <b>glGetTexParameter</b> function returns in <i>params</i> the value or values of the texture parameter specified as <i>pname</i>. The <i>target</i> parameter defines the target texture, either GL_TEXTURE_1D or GL_TEXTURE_2D, to specify one-dimensional or two-dimensional texturing. The <i>pname</i> parameter accepts the same symbols as <a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>, with the same interpretations.

If an error is generated, no change is made to the contents of <i>params</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

