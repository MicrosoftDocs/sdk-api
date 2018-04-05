---
UID: NF:gl.glGetTexLevelParameteriv
title: glGetTexLevelParameteriv function
author: windows-driver-content
description: The glGetTexLevelParameterfv and glGetTexLevelParameteriv functions return texture parameter values for a specific level of detail.
old-location: opengl\glgettexlevelparameteriv.htm
old-project: OpenGL
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_TEXTURE_ALPHA_SIZE, GL_TEXTURE_BLUE_SIZE, GL_TEXTURE_BORDER, GL_TEXTURE_COMPONENTS, GL_TEXTURE_GREEN_SIZE, GL_TEXTURE_HEIGHT, GL_TEXTURE_INTENSITY_SIZE, GL_TEXTURE_INTERNAL_FORMAT, GL_TEXTURE_LUMINANCE_SIZE, GL_TEXTURE_RED_SIZE, GL_TEXTURE_WIDTH, gl/glGetTexLevelParameteriv, glGetTexLevelParameteriv, glGetTexLevelParameteriv function [OpenGL], opengl.glgettexlevelparameteriv
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
-	glGetTexLevelParameteriv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetTexLevelParameteriv function


## -description


The <a href="https://msdn.microsoft.com/5ea91f2e-c0cd-41ee-be95-df096f1c78ef">glGetTexLevelParameterfv</a> and <b>glGetTexLevelParameteriv</b> functions return texture parameter values for a specific level of detail.


## -parameters




### -param target

The symbolic name of the target texture: either GL_TEXTURE_1D, GL_TEXTURE_2D, GL_PROXY_TEXTURE_1D, or GL_PROXY_TEXTURE_2D.


### -param level

The level-of-detail number of the desired image. Level 0 is the base image level. Level <i>n</i> is the <i>n</i>th mipmap reduction image.


### -param pname

The symbolic name of a texture parameter. The following parameter names are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_WIDTH"></a><a id="gl_texture_width"></a><dl>
<dt><b>GL_TEXTURE_WIDTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single value containing the width of the texture image. This value includes the border of the texture image.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_HEIGHT"></a><a id="gl_texture_height"></a><dl>
<dt><b>GL_TEXTURE_HEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single value containing the height of the texture image. This value includes the border of the texture image.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_INTERNAL_FORMAT"></a><a id="gl_texture_internal_format"></a><dl>
<dt><b>GL_TEXTURE_INTERNAL_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single value which describes the texel format of the texture.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_BORDER"></a><a id="gl_texture_border"></a><dl>
<dt><b>GL_TEXTURE_BORDER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single value: the width in pixels of the border of the texture image.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_RED_SIZE"></a><a id="gl_texture_red_size"></a><dl>
<dt><b>GL_TEXTURE_RED_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The internal storage resolution of the red component of a texel. The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GREEN_SIZE"></a><a id="gl_texture_green_size"></a><dl>
<dt><b>GL_TEXTURE_GREEN_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The internal storage resolution of the green component of a texel. The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_BLUE_SIZE"></a><a id="gl_texture_blue_size"></a><dl>
<dt><b>GL_TEXTURE_BLUE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The internal storage resolution of the blue component of a texel. The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_ALPHA_SIZE"></a><a id="gl_texture_alpha_size"></a><dl>
<dt><b>GL_TEXTURE_ALPHA_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The internal storage resolution of the alpha component of a texel. The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_LUMINANCE_SIZE"></a><a id="gl_texture_luminance_size"></a><dl>
<dt><b>GL_TEXTURE_LUMINANCE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The internal storage resolution of the luminance component of a texel. The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_INTENSITY_SIZE"></a><a id="gl_texture_intensity_size"></a><dl>
<dt><b>GL_TEXTURE_INTENSITY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The internal storage resolution of the intensity component of a texel. The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COMPONENTS"></a><a id="gl_texture_components"></a><dl>
<dt><b>GL_TEXTURE_COMPONENTS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single value: the number of components in the texture image.

</td>
</tr>
</table>
 


### -param params

Returns the requested data.


## -returns



This function does not return a value.




## -remarks



The <b>glGetTexLevelParameter</b> function returns in <i>params</i> texture parameter values for a specific level-of-detail value, specified as <i>level</i>. The <i>target</i> parameter defines the target texture, either GL_TEXTURE_1D, GL_TEXTURE_2D, GL_PROXY_TEXTURE_1D, or GL_PROXY_TEXTURE_2D to specify one-dimensional or two-dimensional texturing. The <i>pname</i> parameter specifies the texture parameter whose value or values will be returned.

If an error is generated, no change is made to the contents of <i>params</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

