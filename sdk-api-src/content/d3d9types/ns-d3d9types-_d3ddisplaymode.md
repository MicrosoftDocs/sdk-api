---
UID: NS:d3d9types._D3DDISPLAYMODE
title: "_D3DDISPLAYMODE"
author: windows-driver-content
description: Describes the display mode.
old-location: direct3d9\d3ddisplaymode.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddisplaymode.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 37d3f2f6-71a4-604b-714b-9bd69ecb9f17, D3DDISPLAYMODE, D3DDISPLAYMODE structure [Direct3D 9], LPD3DDISPLAYMODE, LPD3DDISPLAYMODE structure pointer [Direct3D 9], _D3DDISPLAYMODE, d3d9types/D3DDISPLAYMODE, d3d9types/LPD3DDISPLAYMODE, direct3d9.d3ddisplaymode
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
req.typenames: D3DDISPLAYMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDISPLAYMODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDISPLAYMODE structure


## -description


Describes the display mode.


## -struct-fields




### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Screen width, in pixels. 


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Screen height, in pixels. 


### -field RefreshRate

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Refresh rate. The value of 0 indicates an adapter default. 


### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the surface format of the display mode. 


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a>



<a href="https://msdn.microsoft.com/382c327c-dfaa-4ae8-933a-8221a654b7a7">GetAdapterDisplayMode</a>



<a href="https://msdn.microsoft.com/6a96215a-366d-4820-9d9c-440673f1ef75">GetDisplayMode</a>
 

 

