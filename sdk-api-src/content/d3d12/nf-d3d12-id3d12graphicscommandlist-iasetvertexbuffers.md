---
UID: NF:d3d12.ID3D12GraphicsCommandList.IASetVertexBuffers
title: ID3D12GraphicsCommandList::IASetVertexBuffers (d3d12.h)
description: Sets a CPU descriptor handle for the vertex buffers.
helpviewer_keywords: ["IASetVertexBuffers","IASetVertexBuffers method","IASetVertexBuffers method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","IASetVertexBuffers method","ID3D12GraphicsCommandList.IASetVertexBuffers","ID3D12GraphicsCommandList::IASetVertexBuffers","d3d12/ID3D12GraphicsCommandList::IASetVertexBuffers","direct3d12.id3d12graphicscommandlist_iasetvertexbuffers"]
old-location: direct3d12\id3d12graphicscommandlist_iasetvertexbuffers.htm
tech.root: direct3d12
ms.assetid: AADD6CEF-376D-43AB-86E6-37B5D7DD0B25
ms.date: 12/05/2018
ms.keywords: IASetVertexBuffers, IASetVertexBuffers method, IASetVertexBuffers method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,IASetVertexBuffers method, ID3D12GraphicsCommandList.IASetVertexBuffers, ID3D12GraphicsCommandList::IASetVertexBuffers, d3d12/ID3D12GraphicsCommandList::IASetVertexBuffers, direct3d12.id3d12graphicscommandlist_iasetvertexbuffers
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::IASetVertexBuffers
 - d3d12/ID3D12GraphicsCommandList::IASetVertexBuffers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.IASetVertexBuffers
---

# ID3D12GraphicsCommandList::IASetVertexBuffers


## -description

Sets a CPU descriptor handle for the vertex buffers.

## -parameters

### -param StartSlot [in]

Type: <b>UINT</b>

Index into the device's zero-based array to begin setting vertex buffers.

### -param NumViews [in]

Type: <b>UINT</b>

The number of views in the <i>pViews</i> array.

### -param pViews [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view">D3D12_VERTEX_BUFFER_VIEW</a>*</b>

Specifies the vertex buffer views in an array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view">D3D12_VERTEX_BUFFER_VIEW</a> structures.

## -see-also

<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer">IASetIndexBuffer</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>