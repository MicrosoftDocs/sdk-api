---
UID: NF:gl.glTexCoord3dv
title: glTexCoord3dv function
author: windows-driver-content
description: Sets the current texture coordinates.
old-location: opengl\gltexcoord3dv.htm
old-project: OpenGL
ms.assetid: 410f49d6-7950-4940-a377-d62ca2bd5db7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glTexCoord3dv, glTexCoord3dv, glTexCoord3dv function [OpenGL], opengl.gltexcoord3dv
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
-	glTexCoord3dv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTexCoord3dv function


## -description


Sets the current texture coordinates.


## -parameters




### -param v

A pointer to an array of three elements, which in turn specifies the s, t, and r  texture coordinates.


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a> function sets the current texture coordinates that are part of the data associated with polygon vertices.

The <b>glTexCoord</b> function specifies texture coordinates in one, two, three, or four dimensions. The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1). Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q). 

You can update the current texture coordinates  at any time. In particular, you can call glTexCoord  between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>.

The following function retrieves information related to <b>glTexCoord</b>:




<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_CURRENT_TEXTURE_COORDS





## -see-also




<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
 

 

