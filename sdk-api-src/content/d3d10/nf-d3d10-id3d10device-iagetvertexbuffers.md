---
UID: NF:d3d10.ID3D10Device.IAGetVertexBuffers
title: ID3D10Device::IAGetVertexBuffers (d3d10.h)
description: Get the vertex buffers bound to the input-assembler stage. (ID3D10Device.IAGetVertexBuffers)
helpviewer_keywords: ["8b5abcbf-002c-c104-ad3f-1b179ff1df50","IAGetVertexBuffers","IAGetVertexBuffers method [Direct3D 10]","IAGetVertexBuffers method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","IAGetVertexBuffers method","ID3D10Device.IAGetVertexBuffers","ID3D10Device::IAGetVertexBuffers","d3d10/ID3D10Device::IAGetVertexBuffers","direct3d10.id3d10device_iagetvertexbuffers"]
old-location: direct3d10\id3d10device_iagetvertexbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iagetvertexbuffers.htm
ms.date: 12/05/2018
ms.keywords: 8b5abcbf-002c-c104-ad3f-1b179ff1df50, IAGetVertexBuffers, IAGetVertexBuffers method [Direct3D 10], IAGetVertexBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IAGetVertexBuffers method, ID3D10Device.IAGetVertexBuffers, ID3D10Device::IAGetVertexBuffers, d3d10/ID3D10Device::IAGetVertexBuffers, direct3d10.id3d10device_iagetvertexbuffers
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::IAGetVertexBuffers
 - d3d10/ID3D10Device::IAGetVertexBuffers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.IAGetVertexBuffers
---

# ID3D10Device::IAGetVertexBuffers


## -description

Get the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">vertex buffers</a> bound to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage">input-assembler</a> stage.

## -parameters

### -param StartSlot [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">input slot</a> of the first vertex buffer to get. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. A maximum of 16 or 32 input slots (ranges from 0 to either D3D10_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1 or D3D10_1_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">maximum number of input slots depends on the feature level</a>.

### -param NumBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of vertex buffers to get starting at the offset. The number of buffers (plus the starting slot) cannot exceed the total number of IA-stage input slots.

### -param ppVertexBuffers [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>**</b>

A pointer to an array of vertex buffers returned by the method (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>).

### -param pStrides [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to an array of stride values returned by the method; one stride value for each buffer in the vertex-buffer array. Each stride value is the size (in bytes) of the elements that are to be used from that vertex buffer.

### -param pOffsets [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to an array of offset values returned by the method; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
