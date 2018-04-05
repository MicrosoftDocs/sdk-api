---
UID: NS:d3d9types._D3DLOCKED_RECT
title: "_D3DLOCKED_RECT"
author: windows-driver-content
description: Describes a locked rectangular region.
old-location: direct3d9\d3dlocked_rect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dlocked_rect.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 47953486-3317-7f66-0564-fc7b7c0b4d79, D3DLOCKED_RECT, D3DLOCKED_RECT structure [Direct3D 9], LPD3DLOCKED_RECT, LPD3DLOCKED_RECT structure pointer [Direct3D 9], _D3DLOCKED_RECT, d3d9types/D3DLOCKED_RECT, d3d9types/LPD3DLOCKED_RECT, direct3d9.d3dlocked_rect
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
req.typenames: D3DLOCKED_RECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DLOCKED_RECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DLOCKED_RECT structure


## -description


Describes a locked rectangular region.


## -struct-fields




### -field Pitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Number of bytes in one row of the surface.


### -field pBits

Type: <b>void*</b>

Pointer to the locked bits. If a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> was provided to the <a href="https://msdn.microsoft.com/01f5a1a1-e18f-42c9-9654-34e482f48df8">LockRect</a> call, pBits will be appropriately offset from the start of the surface.


## -remarks



The pitch for DXTn formats is different from what was returned in DirectX 7. It now refers to the number of bytes in a row of blocks. For example, if you have a width of 16, then you will have a pitch of 4 blocks (4*8 for DXT1, 4*16 for DXT2-5.)




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/724317a3-1fc7-499d-94b7-759731337a00">IDirect3DCubeTexture9::LockRect</a>



<a href="https://msdn.microsoft.com/01f5a1a1-e18f-42c9-9654-34e482f48df8">IDirect3DSurface9::LockRect</a>



<a href="https://msdn.microsoft.com/b1c3905a-a253-4e3d-b0b2-99c839a5e6d9">IDirect3DTexture9::LockRect</a>
 

 

