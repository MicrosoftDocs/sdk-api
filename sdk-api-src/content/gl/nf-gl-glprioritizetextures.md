---
UID: NF:gl.glPrioritizeTextures
title: glPrioritizeTextures function
author: windows-driver-content
description: The glPrioritizeTextures function sets the residence priority of textures.
old-location: opengl\glprioritizetextures.htm
old-project: OpenGL
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glPrioritizeTextures, gl/glPrioritizeTextures, glPrioritizeTextures, glPrioritizeTextures function [OpenGL], opengl.glprioritizetextures"
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
-	glPrioritizeTextures
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPrioritizeTextures function


## -description


The <b>glPrioritizeTextures</b> function sets the residence priority of textures.


## -parameters




### -param n

The number of textures to be prioritized.


### -param textures

A pointer to the first element of an array containing the names of the textures to be prioritized.


### -param priorities

A pointer to the first element of an array containing the texture priorities. A priority given in an element of the <i>priorities</i> parameter applies to the texture named by the corresponding element of the <i>textures</i> parameter.


## -returns



This function does not return a value.




## -remarks



The <b>glPrioritizeTextures</b> function assigns the <i>n</i> texture priorities specified in the <i>priorities</i> parameter to the <i>n</i> textures named in the <i>textures</i> parameter. On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory. These textures can be bound to a texture target much more efficiently than textures that are not resident.

By specifying a priority for each texture, the <b>glPrioritizeTextures</b> function enables you to determine which textures should be resident.

The texture priorities elements in <i>priorities</i> are clamped to the range [0.0, 1.0] before being assigned. Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident. The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident. However, textures are not guaranteed to be resident until they are bound.

The <b>glPrioritizeTextures</b> function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture. None of the functions named by the <i>textures</i> parameter need to be bound to a texture target.

If a texture is currently bound, you can also use the <a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a> function to set its priority. This is the only way to set the priority of a default texture.

You can include <b>glPrioritizeTextures</b> in display lists.
        

The following function retrieves the priority of a currently-bound texture related to <b>glPrioritizeTextures</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a> with parameter name GL_TEXTURE_PRIORITY</li>
</ul>
<div class="alert"><b>Note</b>  The <b>glPrioritizeTextures</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/55d068a8-d366-4fee-85d5-49373b8c5e02">glAreTexturesResident</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

