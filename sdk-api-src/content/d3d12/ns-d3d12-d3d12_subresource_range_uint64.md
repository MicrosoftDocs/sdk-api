---
UID: NS:d3d12.D3D12_SUBRESOURCE_RANGE_UINT64
title: D3D12_SUBRESOURCE_RANGE_UINT64 (d3d12.h)
description: Describes a subresource memory range.
helpviewer_keywords: ["D3D12_SUBRESOURCE_RANGE_UINT64","D3D12_SUBRESOURCE_RANGE_UINT64 structure","d3d12/D3D12_SUBRESOURCE_RANGE_UINT64","direct3d12.d3d12_subresource_range_uint64"]
old-location: direct3d12\d3d12_subresource_range_uint64.htm
tech.root: direct3d12
ms.assetid: D8DACE22-9AFD-4DCD-A254-A34AD532ACD7
ms.date: 12/05/2018
ms.keywords: D3D12_SUBRESOURCE_RANGE_UINT64, D3D12_SUBRESOURCE_RANGE_UINT64 structure, d3d12/D3D12_SUBRESOURCE_RANGE_UINT64, direct3d12.d3d12_subresource_range_uint64
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
req.typenames: D3D12_SUBRESOURCE_RANGE_UINT64
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SUBRESOURCE_RANGE_UINT64
 - d3d12/D3D12_SUBRESOURCE_RANGE_UINT64
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
 - D3D12_SUBRESOURCE_RANGE_UINT64
---

# D3D12_SUBRESOURCE_RANGE_UINT64 structure


## -description

Describes a subresource memory range.

## -struct-fields

### -field Subresource

The index of the subresource.

### -field Range

A memory range within the subresource.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint">AtomicCopyBufferUINT</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64">AtomicCopyBufferUINT64</a> methods.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>