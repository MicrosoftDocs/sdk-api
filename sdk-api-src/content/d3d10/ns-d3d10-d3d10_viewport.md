---
UID: NS:d3d10.D3D10_VIEWPORT
title: D3D10_VIEWPORT (d3d10.h)
description: Defines the dimensions of a viewport. (D3D10_VIEWPORT)
helpviewer_keywords: ["D3D10_VIEWPORT","D3D10_VIEWPORT structure [Direct3D 10]","d3d10/D3D10_VIEWPORT","direct3d10.d3d10_viewport","fabe1f82-a825-d3c2-8bfb-f2f706d1c57d"]
old-location: direct3d10\d3d10_viewport.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_viewport.htm
ms.date: 12/05/2018
ms.keywords: D3D10_VIEWPORT, D3D10_VIEWPORT structure [Direct3D 10], d3d10/D3D10_VIEWPORT, direct3d10.d3d10_viewport, fabe1f82-a825-d3c2-8bfb-f2f706d1c57d
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D10_VIEWPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_VIEWPORT
 - d3d10/D3D10_VIEWPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_VIEWPORT
---

# D3D10_VIEWPORT structure


## -description

Defines the dimensions of a <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">viewport</a>.

## -struct-fields

### -field TopLeftX

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

X position of the left hand side of the viewport. Ranges between D3D10_VIEWPORT_BOUNDS_MIN and D3D10_VIEWPORT_BOUNDS_MAX.

### -field TopLeftY

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Y position of the top of the viewport. Ranges between D3D10_VIEWPORT_BOUNDS_MIN and D3D10_VIEWPORT_BOUNDS_MAX.

### -field Width

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Width of the viewport.

### -field Height

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Height of the viewport.

### -field MinDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Minimum depth of the viewport. Ranges between 0 and 1.

### -field MaxDepth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Maximum depth of the viewport. Ranges between 0 and 1.

## -remarks

In all cases, <b>Width</b> and <b>Height</b> must be ≥ 0 and <b>TopLeftX</b> + <b>Width</b> and <b>TopLeftY</b> + <b>Height</b> must be ≤ D3D10_VIEWPORT_BOUNDS_MAX.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
