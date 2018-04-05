---
UID: NF:gl.glNormal3b
title: glNormal3b function
author: windows-driver-content
description: Sets the current normal vector.
old-location: opengl\glnormal3b.htm
old-project: OpenGL
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glNormal3b, glNormal3b, glNormal3b function [OpenGL], opengl.glnormal3b
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
-	glNormal3b
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glNormal3b function


## -description


Sets the current normal vector.


## -parameters




### -param nx

Specifies the x-coordinate for the new current normal vector.


### -param ny

Specifies the y-coordinate for the new current normal vector.


### -param nz

Specifies the z-coordinate for the new current normal vector.


## -returns



This function does not return a value.




## -remarks



The current normal is set to the given coordinates whenever you call the <b>glNormal3b</b> function. 

Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.



Normals specified with <b>glNormal3b</b> need not have unit length. If normalization is enabled, then normals specified with <b>glNormal3b</b> are normalized after transformation. You can control normalization by using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> with the argument GL_NORMALIZE. By default, normalization is disabled.

You can update the current normal at any time. In particular, you can call<b>glNormal3b</b>between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>.

The following functions retrieve information related to <b>glNormal3b</b>:




<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_CURRENT_NORMAL


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnable</a> with argument GL_NORMALIZE





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>



<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
 

 

