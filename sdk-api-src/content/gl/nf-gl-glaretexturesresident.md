---
UID: NF:gl.glAreTexturesResident
title: glAreTexturesResident function
author: windows-driver-content
description: The glAreTexturesResident function determines whether specified texture objects are resident in texture memory.
old-location: opengl\glaretexturesresident.htm
old-project: OpenGL
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glAreTexturesResident, gl/glAreTexturesResident, glAreTexturesResident, glAreTexturesResident function [OpenGL], opengl.glaretexturesresident"
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
-	glAreTexturesResident
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glAreTexturesResident function


## -description


The <b>glAreTexturesResident</b> function determines whether specified texture objects are resident in texture memory.


## -parameters




### -param n

The number of textures to be queried.


### -param textures

The address of an array containing the names of the textures to be queried.


### -param residences

The address of an array in which the texture residence status is returned. The residence status of a texture named by an element of <i>textures</i> is returned in the corresponding element of <i>residences</i>.


## -remarks



On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory. These textures can be bound to a texture target much more efficiently than textures that are not resident.

The <b>glAreTexturesResident</b> function queries the texture residence status of the <i>n</i> textures named by the elements of <i>textures</i>. If all the named textures are resident, <b>glAreTexturesResident</b> returns GL_TRUE, and the contents of <i>residences</i> are undisturbed. If any of the named textures are not resident, <b>glAreTexturesResident</b> returns GL_FALSE, and detailed status is returned in the <i>n</i> elements of <i>residences</i>.

If an element of <i>residences</i> is GL_TRUE, then the texture named by the corresponding element of <i>textures</i> is resident in texture memory.

To query the residence status of a single bound texture, call <a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a> with the <i>target</i> parameter set to the target texture to which the target is bound and set the <i>pname</i> parameter to GL_TEXTURE_RESIDENT. You must use this method to query the resident status of a default texture.

You cannot include <b>glAreTexturesResident</b> in display lists.

The <b>glAreTexturesResident</b> function returns the residency status of the textures at the time of invocation. It does not guarantee that the textures will remain resident at any other time.

If textures reside in virtual memory (there is no texture memory), they are considered always resident.

<div class="alert"><b>Note</b>  The <b>glAreTexturesResident</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/800f2360-b40e-4911-9a45-6f310aeeefeb">glBindTexture</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/09018c86-c667-4e43-a95a-51a8077aed33">glPrioritizeTextures</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

