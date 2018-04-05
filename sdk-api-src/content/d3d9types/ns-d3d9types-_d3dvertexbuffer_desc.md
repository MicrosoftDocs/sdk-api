---
UID: NS:d3d9types._D3DVERTEXBUFFER_DESC
title: "_D3DVERTEXBUFFER_DESC"
author: windows-driver-content
description: Describes a vertex buffer.
old-location: direct3d9\d3dvertexbuffer_desc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dvertexbuffer_desc.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 67974a6e-47ed-fc88-12c0-eb5db865b746, D3DVERTEXBUFFER_DESC, D3DVERTEXBUFFER_DESC structure [Direct3D 9], LPD3DVERTEXBUFFER_DESC, LPD3DVERTEXBUFFER_DESC structure pointer [Direct3D 9], _D3DVERTEXBUFFER_DESC, d3d9types/D3DVERTEXBUFFER_DESC, d3d9types/LPD3DVERTEXBUFFER_DESC, direct3d9.d3dvertexbuffer_desc
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
req.typenames: D3DVERTEXBUFFER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DVERTEXBUFFER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DVERTEXBUFFER_DESC structure


## -description


Describes a vertex buffer.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the surface format of the vertex buffer data.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a> enumerated type, identifying this resource as a vertex buffer.


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> flags.


### -field Pool

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, specifying the class of memory allocated for this vertex buffer.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the vertex buffer, in bytes.


### -field FVF

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of <a href="https://msdn.microsoft.com/85d9f5b2-8e4a-4f92-a587-eae5b293778c">D3DFVF</a> that describes the vertex format of the vertices in this buffer.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/1f5842e9-b0ea-460c-998a-24ec024bc561">GetDesc</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

