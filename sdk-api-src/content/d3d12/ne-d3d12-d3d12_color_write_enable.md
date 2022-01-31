---
UID: NE:d3d12.D3D12_COLOR_WRITE_ENABLE
title: D3D12_COLOR_WRITE_ENABLE (d3d12.h)
description: Identifies which components of each pixel of a render target are writable during blending.
helpviewer_keywords: ["D3D12_COLOR_WRITE_ENABLE","D3D12_COLOR_WRITE_ENABLE enumeration","D3D12_COLOR_WRITE_ENABLE_ALL","D3D12_COLOR_WRITE_ENABLE_ALPHA","D3D12_COLOR_WRITE_ENABLE_BLUE","D3D12_COLOR_WRITE_ENABLE_GREEN","D3D12_COLOR_WRITE_ENABLE_RED","d3d12/D3D12_COLOR_WRITE_ENABLE","d3d12/D3D12_COLOR_WRITE_ENABLE_ALL","d3d12/D3D12_COLOR_WRITE_ENABLE_ALPHA","d3d12/D3D12_COLOR_WRITE_ENABLE_BLUE","d3d12/D3D12_COLOR_WRITE_ENABLE_GREEN","d3d12/D3D12_COLOR_WRITE_ENABLE_RED","direct3d12.d3d12_color_write_enable"]
old-location: direct3d12\d3d12_color_write_enable.htm
tech.root: direct3d12
ms.assetid: BC07C5E7-CFEC-4902-9FB1-74A4396190BC
ms.date: 12/05/2018
ms.keywords: D3D12_COLOR_WRITE_ENABLE, D3D12_COLOR_WRITE_ENABLE enumeration, D3D12_COLOR_WRITE_ENABLE_ALL, D3D12_COLOR_WRITE_ENABLE_ALPHA, D3D12_COLOR_WRITE_ENABLE_BLUE, D3D12_COLOR_WRITE_ENABLE_GREEN, D3D12_COLOR_WRITE_ENABLE_RED, d3d12/D3D12_COLOR_WRITE_ENABLE, d3d12/D3D12_COLOR_WRITE_ENABLE_ALL, d3d12/D3D12_COLOR_WRITE_ENABLE_ALPHA, d3d12/D3D12_COLOR_WRITE_ENABLE_BLUE, d3d12/D3D12_COLOR_WRITE_ENABLE_GREEN, d3d12/D3D12_COLOR_WRITE_ENABLE_RED, direct3d12.d3d12_color_write_enable
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
req.typenames: D3D12_COLOR_WRITE_ENABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COLOR_WRITE_ENABLE
 - d3d12/D3D12_COLOR_WRITE_ENABLE
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
 - D3D12_COLOR_WRITE_ENABLE
---

# D3D12_COLOR_WRITE_ENABLE enumeration


## -description

Identifies which components of each pixel of a render target are writable during blending.

## -enum-fields

### -field D3D12_COLOR_WRITE_ENABLE_RED:1

Allow data to be stored in the red component.

### -field D3D12_COLOR_WRITE_ENABLE_GREEN:2

Allow data to be stored in the green component.

### -field D3D12_COLOR_WRITE_ENABLE_BLUE:4

Allow data to be stored in the blue component.

### -field D3D12_COLOR_WRITE_ENABLE_ALPHA:8

Allow data to be stored in the alpha component.

### -field D3D12_COLOR_WRITE_ENABLE_ALL

Allow data to be stored in all components.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc">D3D12_RENDER_TARGET_BLEND_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-blend-desc">CD3DX12_BLEND_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
