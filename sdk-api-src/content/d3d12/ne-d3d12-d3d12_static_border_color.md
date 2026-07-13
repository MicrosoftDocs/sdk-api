---
UID: NE:d3d12.D3D12_STATIC_BORDER_COLOR
title: D3D12_STATIC_BORDER_COLOR (d3d12.h)
description: Specifies the border color for a static sampler.
helpviewer_keywords: ["D3D12_STATIC_BORDER_COLOR","D3D12_STATIC_BORDER_COLOR enumeration","D3D12_STATIC_BORDER_COLOR_OPAQUE_BLACK","D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE","D3D12_STATIC_BORDER_COLOR_TRANSPARENT_BLACK","d3d12/D3D12_STATIC_BORDER_COLOR","d3d12/D3D12_STATIC_BORDER_COLOR_OPAQUE_BLACK","d3d12/D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE","d3d12/D3D12_STATIC_BORDER_COLOR_TRANSPARENT_BLACK","direct3d12.d3d12_static_border_color"]
old-location: direct3d12\d3d12_static_border_color.htm
tech.root: direct3d12
ms.assetid: E5D3E447-F1C7-4AAF-B9AB-829C33622E34
ms.date: 12/05/2018
ms.keywords: D3D12_STATIC_BORDER_COLOR, D3D12_STATIC_BORDER_COLOR enumeration, D3D12_STATIC_BORDER_COLOR_OPAQUE_BLACK, D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, D3D12_STATIC_BORDER_COLOR_TRANSPARENT_BLACK, d3d12/D3D12_STATIC_BORDER_COLOR, d3d12/D3D12_STATIC_BORDER_COLOR_OPAQUE_BLACK, d3d12/D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, d3d12/D3D12_STATIC_BORDER_COLOR_TRANSPARENT_BLACK, direct3d12.d3d12_static_border_color
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
req.typenames: D3D12_STATIC_BORDER_COLOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_STATIC_BORDER_COLOR
 - d3d12/D3D12_STATIC_BORDER_COLOR
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
 - D3D12_STATIC_BORDER_COLOR
---

# D3D12_STATIC_BORDER_COLOR enumeration


## -description

Specifies the border color for a static sampler.

## -enum-fields

### -field D3D12_STATIC_BORDER_COLOR_TRANSPARENT_BLACK:0

Indicates black, with the alpha component as fully transparent.

### -field D3D12_STATIC_BORDER_COLOR_OPAQUE_BLACK

Indicates black, with the alpha component as fully opaque.

### -field D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE

Indicates white, with the alpha component as fully opaque.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc">D3D12_STATIC_SAMPLER_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
