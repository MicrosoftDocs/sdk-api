---
UID: NF:gl.glIsTexture
title: glIsTexture function
author: windows-driver-content
description: The glIsTexture function determines if a name corresponds to a texture.
old-location: opengl\glistexture.htm
old-project: OpenGL
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glIsTexture, gl/glIsTexture, glIsTexture, glIsTexture function [OpenGL], opengl.glistexture"
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
-	glIsTexture
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glIsTexture function


## -description


The <b>glIsTexture</b> function determines if a name corresponds to a texture.


## -parameters




### -param texture

A value that is the name of a texture.


## -remarks



If the <i>texture</i> parameter is currently the name of a texture, the <b>glIsTexture</b> function returns GL_TRUE. The <b>glIsTexture</b> function returns GL_FALSE if <i>texture</i> is zero. It also returns GL_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.

You cannot include calls to <b>glIsTexture</b> in display lists.
        
        

<div class="alert"><b>Note</b>  
        The <b>glIsTexture</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/800f2360-b40e-4911-9a45-6f310aeeefeb">glBindTexture</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/f2491faf-2b33-4b06-9a9f-51ac295690fb">glGenTextures</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

