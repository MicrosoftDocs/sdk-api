---
UID: NF:d3d11.ID3D11DeviceContext.IAGetVertexBuffers
title: ID3D11DeviceContext::IAGetVertexBuffers (d3d11.h)
description: Get the vertex buffers bound to the input-assembler stage. (ID3D11DeviceContext.IAGetVertexBuffers)
helpviewer_keywords: ["IAGetVertexBuffers","IAGetVertexBuffers method [Direct3D 11]","IAGetVertexBuffers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","IAGetVertexBuffers method","ID3D11DeviceContext.IAGetVertexBuffers","ID3D11DeviceContext::IAGetVertexBuffers","d3d11/ID3D11DeviceContext::IAGetVertexBuffers","direct3d11.id3d11devicecontext_iagetvertexbuffers","e62a4871-bb0d-3c8a-9fba-aa0c0dff15b6"]
old-location: direct3d11\id3d11devicecontext_iagetvertexbuffers.htm
tech.root: direct3d11
ms.assetid: 13b1eb06-effa-4483-993a-da47ee0b916f
ms.date: 12/05/2018
ms.keywords: IAGetVertexBuffers, IAGetVertexBuffers method [Direct3D 11], IAGetVertexBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IAGetVertexBuffers method, ID3D11DeviceContext.IAGetVertexBuffers, ID3D11DeviceContext::IAGetVertexBuffers, d3d11/ID3D11DeviceContext::IAGetVertexBuffers, direct3d11.id3d11devicecontext_iagetvertexbuffers, e62a4871-bb0d-3c8a-9fba-aa0c0dff15b6
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::IAGetVertexBuffers
 - d3d11/ID3D11DeviceContext::IAGetVertexBuffers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.IAGetVertexBuffers
---

# ID3D11DeviceContext::IAGetVertexBuffers


## -description

Get the vertex buffers bound to the input-assembler stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The input slot of the first vertex buffer to get. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. The maximum of 16 or 32 input slots (ranges from 0 to D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">maximum number of input slots depends on the feature level</a>.

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of vertex buffers to get starting at the offset. The number of buffers (plus the starting slot) cannot exceed the total number of IA-stage input slots.

### -param ppVertexBuffers [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>**</b>

A pointer to an array of vertex buffers returned by the method (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>).

### -param pStrides [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to an array of stride values returned by the method; one stride value for each buffer in the vertex-buffer array. Each stride value is the size (in bytes) of the elements that are to be used from that vertex buffer.

### -param pOffsets [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to an array of offset values returned by the method; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
