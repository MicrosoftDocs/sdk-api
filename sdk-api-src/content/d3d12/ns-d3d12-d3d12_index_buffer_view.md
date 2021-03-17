---
UID: NS:d3d12.D3D12_INDEX_BUFFER_VIEW
title: D3D12_INDEX_BUFFER_VIEW (d3d12.h)
description: Describes the index buffer to view.
helpviewer_keywords: ["D3D12_INDEX_BUFFER_VIEW","D3D12_INDEX_BUFFER_VIEW structure","d3d12/D3D12_INDEX_BUFFER_VIEW","direct3d12.d3d12_index_buffer_view"]
old-location: direct3d12\d3d12_index_buffer_view.htm
tech.root: direct3d12
ms.assetid: CADD98BF-EDA9-43D6-9ADA-392051541B61
ms.date: 12/05/2018
ms.keywords: D3D12_INDEX_BUFFER_VIEW, D3D12_INDEX_BUFFER_VIEW structure, d3d12/D3D12_INDEX_BUFFER_VIEW, direct3d12.d3d12_index_buffer_view
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_INDEX_BUFFER_VIEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_INDEX_BUFFER_VIEW
 - d3d12/D3D12_INDEX_BUFFER_VIEW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_INDEX_BUFFER_VIEW
---

# D3D12_INDEX_BUFFER_VIEW structure


## -description

Describes the index buffer to view.

## -struct-fields

### -field BufferLocation

The GPU virtual address of the index buffer.  
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd synonym of UINT64.

### -field SizeInBytes

The size in bytes of the index buffer.

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the index-buffer format.

## -remarks

This structure is passed into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer">ID3D12GraphicsCommandList::IASetIndexBuffer</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>