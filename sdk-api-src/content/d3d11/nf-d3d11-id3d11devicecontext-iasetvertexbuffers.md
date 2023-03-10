---
UID: NF:d3d11.ID3D11DeviceContext.IASetVertexBuffers
title: ID3D11DeviceContext::IASetVertexBuffers (d3d11.h)
description: Bind an array of vertex buffers to the input-assembler stage. (ID3D11DeviceContext.IASetVertexBuffers)
helpviewer_keywords: ["IASetVertexBuffers","IASetVertexBuffers method [Direct3D 11]","IASetVertexBuffers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","IASetVertexBuffers method","ID3D11DeviceContext.IASetVertexBuffers","ID3D11DeviceContext::IASetVertexBuffers","d3b78697-f1d6-7517-a7bb-93d9f91ac800","d3d11/ID3D11DeviceContext::IASetVertexBuffers","direct3d11.id3d11devicecontext_iasetvertexbuffers"]
old-location: direct3d11\id3d11devicecontext_iasetvertexbuffers.htm
tech.root: direct3d11
ms.assetid: e9a9a69c-7df7-4784-98f5-9ad63f6cd407
ms.date: 12/05/2018
ms.keywords: IASetVertexBuffers, IASetVertexBuffers method [Direct3D 11], IASetVertexBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IASetVertexBuffers method, ID3D11DeviceContext.IASetVertexBuffers, ID3D11DeviceContext::IASetVertexBuffers, d3b78697-f1d6-7517-a7bb-93d9f91ac800, d3d11/ID3D11DeviceContext::IASetVertexBuffers, direct3d11.id3d11devicecontext_iasetvertexbuffers
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
 - ID3D11DeviceContext::IASetVertexBuffers
 - d3d11/ID3D11DeviceContext::IASetVertexBuffers
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
 - ID3D11DeviceContext.IASetVertexBuffers
---

# ID3D11DeviceContext::IASetVertexBuffers


## -description

Bind an array of vertex buffers to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler stage</a>.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The first input slot for binding. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. The maximum of 16 or 32 input slots (ranges from 0 to D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">maximum number of input slots depends on the feature level</a>.

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of vertex buffers in the array. The number of buffers (plus the starting slot) can't exceed the total number of IA-stage input slots (ranges from 0 to D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - StartSlot).

### -param ppVertexBuffers [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

A pointer to an array of vertex buffers (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>). The vertex buffers must have been created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_VERTEX_BUFFER</a> flag.

### -param pStrides [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to an array of stride values; one stride value for each buffer in the vertex-buffer array. Each stride is the size (in bytes) of the elements that are to be used from that vertex buffer.

### -param pOffsets [in, optional]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to an array of offset values; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.

## -remarks

For info about creating vertex buffers, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to">How to: Create a Vertex Buffer</a>.
        

Calling this method using a buffer that is currently bound for writing (that is, bound to the stream output pipeline stage) will effectively bind <b>NULL</b> instead because a buffer can't be bound as both an input and an output at the same time.
        

The debug layer will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
