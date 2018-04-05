---
UID: NS:d3d9types._D3DLOCKED_BOX
title: "_D3DLOCKED_BOX"
author: windows-driver-content
description: Describes a locked box (volume).
old-location: direct3d9\d3dlocked_box.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dlocked_box.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 50598771-9d0a-d3a9-0987-4733e7b51f9b, D3DLOCKED_BOX, D3DLOCKED_BOX structure [Direct3D 9], LPD3DLOCKED_BOX, LPD3DLOCKED_BOX structure pointer [Direct3D 9], _D3DLOCKED_BOX, d3d9types/D3DLOCKED_BOX, d3d9types/LPD3DLOCKED_BOX, direct3d9.d3dlocked_box
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
req.typenames: D3DLOCKED_BOX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DLOCKED_BOX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DLOCKED_BOX structure


## -description


Describes a locked box (volume).


## -struct-fields




### -field RowPitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">int</a></b>

Byte offset from the left edge of one row to the left edge of the next row.


### -field SlicePitch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">int</a></b>

Byte offset from the top-left of one slice to the top-left of the next deepest slice. 


### -field pBits

Type: <b>void*</b>

Pointer to the beginning of the volume box. If a <a href="https://msdn.microsoft.com/415a96bc-1621-4691-b87a-98ca22f0bf07">D3DBOX</a> was provided to the LockBox call, pBits will be appropriately offset from the start of the volume. 


## -remarks



Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume. For more information, see <a href="https://msdn.microsoft.com/1d692501-a524-4ad4-8779-d71f1bda7bc9">Volume Texture Resources (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/055f3e52-30f6-4fbe-90a0-e56ac0ebe3ca">IDirect3DVolume9::LockBox</a>



<a href="https://msdn.microsoft.com/732f7711-a71b-4470-824e-4ea0b47e64f7">IDirect3DVolumeTexture9::LockBox</a>
 

 

