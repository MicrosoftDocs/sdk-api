---
UID: NF:gl.glGenTextures
title: glGenTextures function
author: windows-driver-content
description: The glGenTextures function generates texture names.
old-location: opengl\glgentextures.htm
old-project: OpenGL
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGenTextures, gl/glGenTextures, glGenTextures, glGenTextures function [OpenGL], opengl.glgentextures"
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
-	glGenTextures
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGenTextures function


## -description


The <b>glGenTextures</b> function generates texture names.


## -parameters




### -param n

The number of texture names to be generated.


### -param textures

A pointer to the first element of an array in which the generated texture names are stored.


## -returns



This function does not return a value.




## -remarks



The <b>glGenTextures</b> function returns <i>n</i> texture names in the <i>textures</i> parameter. The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the <b>glGenTextures</b> function. The generated textures assume the dimensionality of the texture target to which they are first bound with the <a href="https://msdn.microsoft.com/800f2360-b40e-4911-9a45-6f310aeeefeb">glBindTexture</a> function. Texture names returned by <b>glGenTextures</b> are not returned by subsequent calls to <b>glGenTextures</b> unless they are first deleted by calling <a href="https://msdn.microsoft.com/300eb99a-9ee5-4495-9489-7e084db9c6c1">glDeleteTextures</a>.

You cannot include <b>glGenTextures</b> in display lists.

<div class="alert"><b>Note</b>  The <b>glGenTextures</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>
The following function retrieves information related to <b>glGenTextures</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/89d06642-ff28-4a67-ac7f-ca58150f301e">glIsTexture</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/800f2360-b40e-4911-9a45-6f310aeeefeb">glBindTexture</a>



<a href="https://msdn.microsoft.com/300eb99a-9ee5-4495-9489-7e084db9c6c1">glDeleteTextures</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/89d06642-ff28-4a67-ac7f-ca58150f301e">glIsTexture</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

