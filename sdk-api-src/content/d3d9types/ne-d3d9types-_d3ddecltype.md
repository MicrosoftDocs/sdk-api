---
UID: NE:d3d9types._D3DDECLTYPE
title: "_D3DDECLTYPE"
author: windows-driver-content
description: Defines a vertex declaration data type.
old-location: direct3d9\D3DDECLTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddecltype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DDECLTYPE, D3DDECLTYPE enumeration [Direct3D 9], D3DDECLTYPE_D3DCOLOR, D3DDECLTYPE_DEC3N, D3DDECLTYPE_FLOAT1, D3DDECLTYPE_FLOAT16_2, D3DDECLTYPE_FLOAT16_4, D3DDECLTYPE_FLOAT2, D3DDECLTYPE_FLOAT3, D3DDECLTYPE_FLOAT4, D3DDECLTYPE_SHORT2, D3DDECLTYPE_SHORT2N, D3DDECLTYPE_SHORT4, D3DDECLTYPE_SHORT4N, D3DDECLTYPE_UBYTE4, D3DDECLTYPE_UBYTE4N, D3DDECLTYPE_UDEC3, D3DDECLTYPE_UNUSED, D3DDECLTYPE_USHORT2N, D3DDECLTYPE_USHORT4N, LPD3DDECLTYPE, LPD3DDECLTYPE enumeration pointer [Direct3D 9], _D3DDECLTYPE, b4dea636-8987-fe65-2c1e-0b08ea1ffddb, d3d9types/D3DDECLTYPE, d3d9types/D3DDECLTYPE_D3DCOLOR, d3d9types/D3DDECLTYPE_DEC3N, d3d9types/D3DDECLTYPE_FLOAT1, d3d9types/D3DDECLTYPE_FLOAT16_2, d3d9types/D3DDECLTYPE_FLOAT16_4, d3d9types/D3DDECLTYPE_FLOAT2, d3d9types/D3DDECLTYPE_FLOAT3, d3d9types/D3DDECLTYPE_FLOAT4, d3d9types/D3DDECLTYPE_SHORT2, d3d9types/D3DDECLTYPE_SHORT2N, d3d9types/D3DDECLTYPE_SHORT4, d3d9types/D3DDECLTYPE_SHORT4N, d3d9types/D3DDECLTYPE_UBYTE4, d3d9types/D3DDECLTYPE_UBYTE4N, d3d9types/D3DDECLTYPE_UDEC3, d3d9types/D3DDECLTYPE_UNUSED, d3d9types/D3DDECLTYPE_USHORT2N, d3d9types/D3DDECLTYPE_USHORT4N, d3d9types/LPD3DDECLTYPE, direct3d9.D3DDECLTYPE
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
req.typenames: D3DDECLTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDECLTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDECLTYPE enumeration


## -description


Defines a vertex declaration data type.


## -enum-fields




### -field D3DDECLTYPE_FLOAT1

One-component float expanded to (float, 0, 0, 1).


### -field D3DDECLTYPE_FLOAT2

Two-component float expanded to (float, float, 0, 1).


### -field D3DDECLTYPE_FLOAT3

Three-component float expanded to (float, float, float, 1).


### -field D3DDECLTYPE_FLOAT4

Four-component float expanded to (float, float, float, float).


### -field D3DDECLTYPE_D3DCOLOR

Four-component, packed, unsigned bytes mapped to 0 to 1 range. Input is a <a href="https://msdn.microsoft.com/a4425774-fd4b-4f5c-9e10-7679bc2795f6">D3DCOLOR</a> and is expanded to RGBA order.


### -field D3DDECLTYPE_UBYTE4

Four-component, unsigned byte.


### -field D3DDECLTYPE_SHORT2

Two-component, signed short expanded to (value, value, 0, 1).


### -field D3DDECLTYPE_SHORT4

Four-component, signed short expanded to (value, value, value, value).


### -field D3DDECLTYPE_UBYTE4N

Four-component byte with each byte normalized by dividing with 255.0f.


### -field D3DDECLTYPE_SHORT2N

Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1). 


### -field D3DDECLTYPE_SHORT4N

Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0). 


### -field D3DDECLTYPE_USHORT2N

Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1). 


### -field D3DDECLTYPE_USHORT4N

Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0). 


### -field D3DDECLTYPE_UDEC3

Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).


### -field D3DDECLTYPE_DEC3N

Three-component, signed, 10 10 10 format normalized and expanded to (v[0]/511.0, v[1]/511.0, v[2]/511.0, 1). 


### -field D3DDECLTYPE_FLOAT16_2

Two-component, 16-bit, floating point expanded to (value, value, 0, 1).


### -field D3DDECLTYPE_FLOAT16_4

Four-component, 16-bit, floating point expanded to (value, value, value, value). 


### -field D3DDECLTYPE_UNUSED

Type field in the declaration is unused. This is designed for use with D3DDECLMETHOD_UV  and D3DDECLMETHOD_LOOKUPPRESAMPLED.


## -remarks



Vertex data is declared with an array of <a href="https://msdn.microsoft.com/6f3c40a0-b28e-48d6-acad-ef80a919c5d7">D3DVERTEXELEMENT9</a> structures. Each element in the array contains a vertex declaration data type.

Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device. You can get this tool and learn about it from the DirectX SDK. For info about the DirectX SDK, see <a href="https://msdn.microsoft.com/d8765da9-e7cf-47e8-8bc3-4b29162da41b">Where is the DirectX SDK?</a>.




## -see-also




<a href="https://msdn.microsoft.com/030e04a6-4e2d-4756-80ef-e4a6a0103fd1">D3DDECLMETHOD</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

