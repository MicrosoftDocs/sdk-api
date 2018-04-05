---
UID: NF:gl.glGetTexEnviv
title: glGetTexEnviv function
author: windows-driver-content
description: The glGetTexEnvfv and glGetTexEnviv functions return texture environment parameters.
old-location: opengl\glgettexenviv.htm
old-project: OpenGL
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_TEXTURE_ENV_COLOR, GL_TEXTURE_ENV_MODE, gl/glGetTexEnviv, glGetTexEnviv, glGetTexEnviv function [OpenGL], opengl.glgettexenviv
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
-	glGetTexEnviv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetTexEnviv function


## -description


The <a href="https://msdn.microsoft.com/aa037494-e227-48f1-8d5e-9f82073dc2ea">glGetTexEnvfv</a> and <b>glGetTexEnviv</b> functions return texture environment parameters.


## -parameters




### -param target

A texture environment. Must be GL_TEXTURE_ENV.


### -param pname

The symbolic name of a texture environment parameter. The following values are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_ENV_MODE"></a><a id="gl_texture_env_mode"></a><dl>
<dt><b>GL_TEXTURE_ENV_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns the single-valued texture environment mode, a symbolic constant.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_ENV_COLOR"></a><a id="gl_texture_env_color"></a><dl>
<dt><b>GL_TEXTURE_ENV_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four integer or floating-point values that are the texture environment color. Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.

</td>
</tr>
</table>
 


### -param params

Returns the requested data.


## -returns



This function does not return a value.




## -remarks



The <b>glGetTexEnv</b> function returns in <i>params</i> selected values of a texture environment that was specified with <a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>. The <i>target</i> parameter specifies a texture environment. Currently, only one texture environment is defined and supported: GL_TEXTURE_ENV.

The <i>pname</i> parameter names a specific texture environment parameter.

If an error is generated, no change is made to the contents of <i>params</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>
 

 

