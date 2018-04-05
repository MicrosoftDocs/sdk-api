---
UID: NS:d3d9types.D3DDISPLAYMODEEX
title: D3DDISPLAYMODEEX
author: windows-driver-content
description: Information about the properties of a display mode.
old-location: direct3d9\d3ddisplaymodeex.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddisplaymodeex.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 5ed08b0c-7c20-365e-7985-bca4439f7ae8, D3DDISPLAYMODEEX, D3DDISPLAYMODEEX structure [Direct3D 9], d3d9types/D3DDISPLAYMODEEX, direct3d9.d3ddisplaymodeex
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
req.typenames: D3DDISPLAYMODEEX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DDISPLAYMODEEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DDISPLAYMODEEX structure


## -description


Information about the properties of a display mode.


## -struct-fields




### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of this structure. This should always be set to sizeof(D3DDISPLAYMODEEX).


### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the display mode.


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the display mode.


### -field RefreshRate

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Refresh rate of the display mode.


### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Format of the display mode. See <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>.


### -field ScanLineOrdering

Type: <b><a href="https://msdn.microsoft.com/55cf790e-ebe9-4791-a2be-a90fc76bae57">D3DSCANLINEORDERING</a></b>

Indicates whether the scanline order is progressive or interlaced. See <a href="https://msdn.microsoft.com/55cf790e-ebe9-4791-a2be-a90fc76bae57">D3DSCANLINEORDERING</a>.


## -remarks



This structure is used in various methods to create and manage Direct3D 9Ex devices (<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>) and swapchains (<a href="https://msdn.microsoft.com/b5af736b-f1d6-4db2-bd57-d88fca65b0a6">IDirect3DSwapChain9Ex</a>).




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

