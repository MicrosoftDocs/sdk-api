---
UID: NS:d3d9types._D3DVIEWPORT9
title: "_D3DVIEWPORT9"
author: windows-driver-content
description: Defines the window dimensions of a render-target surface onto which a 3D volume projects.
old-location: direct3d9\d3dviewport9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dviewport9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DVIEWPORT9, D3DVIEWPORT9 structure [Direct3D 9], LPD3DVIEWPORT9, LPD3DVIEWPORT9 structure pointer [Direct3D 9], _D3DVIEWPORT9, d3d9types/D3DVIEWPORT9, d3d9types/LPD3DVIEWPORT9, direct3d9.d3dviewport9, fc4c36aa-f2f3-0ab1-c806-68e3b3ac2d50
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DVIEWPORT9
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DVIEWPORT9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DVIEWPORT9 structure


## -description


Defines the window dimensions of a render-target surface onto which a 3D volume projects.


## -struct-fields




### -field X

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Pixel coordinate of the upper-left corner of the viewport on the render-target surface. Unless you want to render to a subset of the surface, this member can be set to 0. 


### -field Y

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Pixel coordinate of the upper-left corner of the viewport on the render-target surface. Unless you want to render to a subset of the surface, this member can be set to 0. 


### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Width dimension of the clip volume, in pixels. Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface. 


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Height dimension of the clip volume, in pixels. Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface. 


### -field MinZ

Type: <b>float</b>

Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume. Most applications set this value to 0.0. Clipping is performed after applying the projection matrix. 


### -field MaxZ

Type: <b>float</b>

Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume. Most applications set this value to 1.0. Clipping is performed after applying the projection matrix. 


## -remarks



The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface. Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively. The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects. For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.
    


When the viewport parameters for a device change (because of a call to the <a href="https://msdn.microsoft.com/57fd3a83-4bb4-4f6c-9233-d65208d4bb39">SetViewport</a> method), the driver builds a new transformation matrix.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/026da206-b2e7-421c-92f8-344fef7ad245">GetViewport</a>



<a href="https://msdn.microsoft.com/57fd3a83-4bb4-4f6c-9233-d65208d4bb39">SetViewport</a>
 

 

