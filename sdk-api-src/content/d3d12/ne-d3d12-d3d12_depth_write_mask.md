---
UID: NE:d3d12.D3D12_DEPTH_WRITE_MASK
title: D3D12_DEPTH_WRITE_MASK (d3d12.h)
description: Identifies the portion of a depth-stencil buffer for writing depth data.
helpviewer_keywords: ["D3D12_DEPTH_WRITE_MASK","D3D12_DEPTH_WRITE_MASK enumeration","D3D12_DEPTH_WRITE_MASK_ALL","D3D12_DEPTH_WRITE_MASK_ZERO","d3d12/D3D12_DEPTH_WRITE_MASK","d3d12/D3D12_DEPTH_WRITE_MASK_ALL","d3d12/D3D12_DEPTH_WRITE_MASK_ZERO","direct3d12.d3d12_depth_write_mask"]
old-location: direct3d12\d3d12_depth_write_mask.htm
tech.root: direct3d12
ms.assetid: 28037BEA-3525-4EBC-973B-421C77629ECB
ms.date: 12/05/2018
ms.keywords: D3D12_DEPTH_WRITE_MASK, D3D12_DEPTH_WRITE_MASK enumeration, D3D12_DEPTH_WRITE_MASK_ALL, D3D12_DEPTH_WRITE_MASK_ZERO, d3d12/D3D12_DEPTH_WRITE_MASK, d3d12/D3D12_DEPTH_WRITE_MASK_ALL, d3d12/D3D12_DEPTH_WRITE_MASK_ZERO, direct3d12.d3d12_depth_write_mask
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
req.typenames: D3D12_DEPTH_WRITE_MASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEPTH_WRITE_MASK
 - d3d12/D3D12_DEPTH_WRITE_MASK
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
 - D3D12_DEPTH_WRITE_MASK
---

# D3D12_DEPTH_WRITE_MASK enumeration


## -description

Identifies the portion of a depth-stencil buffer for writing depth data.

## -enum-fields

### -field D3D12_DEPTH_WRITE_MASK_ZERO:0

Turn off writes to the depth-stencil buffer.

### -field D3D12_DEPTH_WRITE_MASK_ALL:1

Turn on writes to the depth-stencil buffer.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc">D3D12_DEPTH_STENCIL_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-depth-stencil-desc">CD3DX12_DEPTH_STENCIL_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
