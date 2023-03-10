---
UID: NE:d3d12.D3D12_RESOLVE_MODE
title: D3D12_RESOLVE_MODE (d3d12.h)
description: Specifies a resolve operation.
helpviewer_keywords: ["D3D12_RESOLVE_MODE","D3D12_RESOLVE_MODE enumeration","D3D12_RESOLVE_MODE_AVERAGE","D3D12_RESOLVE_MODE_DECOMPRESS","D3D12_RESOLVE_MODE_MAX","D3D12_RESOLVE_MODE_MIN","d3d12/D3D12_RESOLVE_MODE","d3d12/D3D12_RESOLVE_MODE_AVERAGE","d3d12/D3D12_RESOLVE_MODE_DECOMPRESS","d3d12/D3D12_RESOLVE_MODE_MAX","d3d12/D3D12_RESOLVE_MODE_MIN","direct3d12.d3d12_resolve_mode"]
old-location: direct3d12\d3d12_resolve_mode.htm
tech.root: direct3d12
ms.assetid: 1E14F62A-E6B9-4C88-AC28-2322C4662E1F
ms.date: 12/05/2018
ms.keywords: D3D12_RESOLVE_MODE, D3D12_RESOLVE_MODE enumeration, D3D12_RESOLVE_MODE_AVERAGE, D3D12_RESOLVE_MODE_DECOMPRESS, D3D12_RESOLVE_MODE_MAX, D3D12_RESOLVE_MODE_MIN, d3d12/D3D12_RESOLVE_MODE, d3d12/D3D12_RESOLVE_MODE_AVERAGE, d3d12/D3D12_RESOLVE_MODE_DECOMPRESS, d3d12/D3D12_RESOLVE_MODE_MAX, d3d12/D3D12_RESOLVE_MODE_MIN, direct3d12.d3d12_resolve_mode
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
req.typenames: D3D12_RESOLVE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOLVE_MODE
 - d3d12/D3D12_RESOLVE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RESOLVE_MODE
---

# D3D12_RESOLVE_MODE enumeration


## -description

Specifies a resolve operation.

## -enum-fields

### -field D3D12_RESOLVE_MODE_DECOMPRESS:0

Resolves compressed source samples to their uncompressed values. When using this operation, the source and destination resources must have the same sample count, unlike the min, max, and average operations that require the destination to have a sample count of 1.

### -field D3D12_RESOLVE_MODE_MIN:1

Resolves the source samples to their minimum value. It can be used with any render target or depth stencil format.

### -field D3D12_RESOLVE_MODE_MAX:2

Resolves the source samples to their maximum value. It can be used with any render target or depth stencil format.

### -field D3D12_RESOLVE_MODE_AVERAGE:3

Resolves the source samples to their average value. It can be used with any non-integer render target format, including the depth plane. It can't be used with integer render target formats, including the stencil plane.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion">ID3D12GraphicsCommandList1::ResolveSubresourceRegion</a> function.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
