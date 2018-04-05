---
UID: NE:d3d9types._D3DRESOURCETYPE
title: "_D3DRESOURCETYPE"
author: windows-driver-content
description: Defines resource types.
old-location: direct3d9\D3DRESOURCETYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dresourcetype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 04422352-cd15-9d2a-8627-0dac03c6a6b2, D3DRESOURCETYPE, D3DRESOURCETYPE enumeration [Direct3D 9], D3DRTYPE_CubeTexture, D3DRTYPE_FORCE_DWORD, D3DRTYPE_INDEXBUFFER, D3DRTYPE_SURFACE, D3DRTYPE_TEXTURE, D3DRTYPE_VERTEXBUFFER, D3DRTYPE_VOLUME, D3DRTYPE_VOLUMETEXTURE, LPD3DRESOURCETYPE, LPD3DRESOURCETYPE enumeration pointer [Direct3D 9], _D3DRESOURCETYPE, d3d9types/D3DRESOURCETYPE, d3d9types/D3DRTYPE_CubeTexture, d3d9types/D3DRTYPE_FORCE_DWORD, d3d9types/D3DRTYPE_INDEXBUFFER, d3d9types/D3DRTYPE_SURFACE, d3d9types/D3DRTYPE_TEXTURE, d3d9types/D3DRTYPE_VERTEXBUFFER, d3d9types/D3DRTYPE_VOLUME, d3d9types/D3DRTYPE_VOLUMETEXTURE, d3d9types/LPD3DRESOURCETYPE, direct3d9.D3DRESOURCETYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3DRESOURCETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DRESOURCETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DRESOURCETYPE enumeration


## -description


Defines resource types.


## -enum-fields




### -field D3DRTYPE_SURFACE

Surface resource. 


### -field D3DRTYPE_VOLUME

Volume resource. 


### -field D3DRTYPE_TEXTURE

Texture resource. 


### -field D3DRTYPE_VOLUMETEXTURE

Volume texture resource. 


### -field D3DRTYPE_CUBETEXTURE


### -field D3DRTYPE_VERTEXBUFFER

Vertex buffer resource. 


### -field D3DRTYPE_INDEXBUFFER

Index buffer resource. 


### -field D3DRTYPE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


#### - D3DRTYPE_CubeTexture

Cube texture resource. 


## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/4126cd36-34e5-4224-8b62-54b090322ddc">IDirect3DResource9::GetType</a>
 

 

