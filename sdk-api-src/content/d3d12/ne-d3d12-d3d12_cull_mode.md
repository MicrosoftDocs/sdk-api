---
UID: NE:d3d12.D3D12_CULL_MODE
title: D3D12_CULL_MODE (d3d12.h)
description: Specifies triangles facing a particular direction are not drawn.
helpviewer_keywords: ["D3D12_CULL_MODE","D3D12_CULL_MODE enumeration","D3D12_CULL_MODE_BACK","D3D12_CULL_MODE_FRONT","D3D12_CULL_MODE_NONE","d3d12/D3D12_CULL_MODE","d3d12/D3D12_CULL_MODE_BACK","d3d12/D3D12_CULL_MODE_FRONT","d3d12/D3D12_CULL_MODE_NONE","direct3d12.d3d12_cull_mode"]
old-location: direct3d12\d3d12_cull_mode.htm
tech.root: direct3d12
ms.assetid: C605D9C3-6188-4307-81C0-753D2043EF4E
ms.date: 12/05/2018
ms.keywords: D3D12_CULL_MODE, D3D12_CULL_MODE enumeration, D3D12_CULL_MODE_BACK, D3D12_CULL_MODE_FRONT, D3D12_CULL_MODE_NONE, d3d12/D3D12_CULL_MODE, d3d12/D3D12_CULL_MODE_BACK, d3d12/D3D12_CULL_MODE_FRONT, d3d12/D3D12_CULL_MODE_NONE, direct3d12.d3d12_cull_mode
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
req.typenames: D3D12_CULL_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CULL_MODE
 - d3d12/D3D12_CULL_MODE
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
 - D3D12_CULL_MODE
---

# D3D12_CULL_MODE enumeration


## -description

Specifies triangles facing a particular direction are not drawn.

## -enum-fields

### -field D3D12_CULL_MODE_NONE:1

Always draw all triangles.

### -field D3D12_CULL_MODE_FRONT:2

Do not draw triangles that are front-facing.

### -field D3D12_CULL_MODE_BACK:3

Do not draw triangles that are back-facing.

## -remarks

Cull mode is specified in a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc">D3D12_RASTERIZER_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-rasterizer-desc">CD3DX12_RASTERIZER_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
