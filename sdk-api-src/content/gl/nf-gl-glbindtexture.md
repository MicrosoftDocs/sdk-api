---
UID: NF:gl.glBindTexture
title: glBindTexture function
author: windows-driver-content
description: The glBindTexture function enables the creation of a named texture that is bound to a texture target.
old-location: opengl\glbindtexture.htm
old-project: OpenGL
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glBindTexture, gl/glBindTexture, glBindTexture, glBindTexture function [OpenGL], opengl.glbindtexture"
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
-	opengl32.dll
api_name:
-	glBindTexture
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glBindTexture function


## -description


The <b>glBindTexture</b> function enables the creation of a named texture that is bound to a texture target.


## -parameters




### -param target

The target to which the texture is bound. Must have the value GL_TEXTURE_1D or GL_TEXTURE_2D.


### -param texture

The name of a texture; the texture name cannot currently be in use.


## -returns



This function does not return a value.




## -remarks



The <b>glBindTexture</b> function enables you to create a named texture. 
      Calling <b>glBindTexture</b> with <i>target</i> set to GL_TEXTURE_1D or GL_TEXTURE_2D, and <i>texture</i> set
      to the name of the new texture you have created binds the texture name to the appropriate texture target. When a texture is bound to a target, the previous binding for that target is no longer in effect.

Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target. Texture names and the corresponding texture contents are local to the
      shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists. You can generate a set of new texture names
      using <a href="https://msdn.microsoft.com/f2491faf-2b33-4b06-9a9f-51ac295690fb">glGenTextures</a>.

When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL_TEXTURE_1D becomes one-dimensional and a texture bound to GL_TEXTURE_2D becomes 
      two-dimensional. Operations you perform on a texture target also affect a texture bound to the target. When you query a texture target, the return value is the state of the texture bound to it. 
      Texture targets become aliases for textures currently bound to them.

When you bind a texture with <b>glBindTexture</b>, the binding remains active until a different texture is bound to the same target or
      you delete the bound texture with the <a href="https://msdn.microsoft.com/300eb99a-9ee5-4495-9489-7e084db9c6c1">glDeleteTextures</a> function. Once you create a named texture you can bind it to a texture target 
      that has the same dimensionality as often as needed.

It is usually much faster to use <b>glBindTexture</b> to bind an existing named texture to one of the texture targets than it is to 
      reload the texture image using <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>. 
      For additional control of texturing performance, use <a href="https://msdn.microsoft.com/09018c86-c667-4e43-a95a-51a8077aed33">glPrioritizeTextures</a>.

You can include calls to <b>glBindTexture</b> in display lists.

<div class="alert"><b>Note</b>  The <b>glBindTexture</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>
The following functions retrieve information related to <b>glBindTexture</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_TEXTURE_1D_BINDING</li>
</ul>
<b>glGet</b> with argument GL_TEXTURE_2D_BINDING




## -see-also




<a href="https://msdn.microsoft.com/55d068a8-d366-4fee-85d5-49373b8c5e02">glAreTexturesResident</a>



<a href="https://msdn.microsoft.com/300eb99a-9ee5-4495-9489-7e084db9c6c1">glDeleteTextures</a>



<a href="https://msdn.microsoft.com/f2491faf-2b33-4b06-9a9f-51ac295690fb">glGenTextures</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/89d06642-ff28-4a67-ac7f-ca58150f301e">glIsTexture</a>



<a href="https://msdn.microsoft.com/09018c86-c667-4e43-a95a-51a8077aed33">glPrioritizeTextures</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

