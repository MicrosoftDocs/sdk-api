---
UID: NS:d3d12.D3D12_RANGE
title: D3D12_RANGE (d3d12.h)
description: Describes a memory range.
helpviewer_keywords: ["D3D12_RANGE","D3D12_RANGE structure","d3d12/D3D12_RANGE","direct3d12.d3d12_range"]
old-location: direct3d12\d3d12_range.htm
tech.root: direct3d12
ms.assetid: E8A66EC7-DB20-475D-BCD1-6C164FF39D24
ms.date: 12/05/2018
ms.keywords: D3D12_RANGE, D3D12_RANGE structure, d3d12/D3D12_RANGE, direct3d12.d3d12_range
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
req.typenames: D3D12_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RANGE
 - d3d12/D3D12_RANGE
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
 - D3D12_RANGE
---

# D3D12_RANGE structure


## -description

Describes a memory range.

## -struct-fields

### -field Begin

The offset, in bytes, denoting the beginning of a memory range.

### -field End

The offset, in bytes, denoting the end of a memory range.
            <b>End</b> is one-past-the-end.

## -remarks

<b>End</b> is one-past-the-end.
        When <b>Begin</b> equals <b>End</b>, the range is empty.
        The size of the range is (<b>End</b> - <b>Begin</b>).
      

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map">Map</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap">Unmap</a> methods.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-range">CD3DX12_RANGE</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>