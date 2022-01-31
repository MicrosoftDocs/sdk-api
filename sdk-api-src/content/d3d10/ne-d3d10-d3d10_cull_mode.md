---
UID: NE:d3d10.D3D10_CULL_MODE
title: D3D10_CULL_MODE (d3d10.h)
description: Indicates triangles facing a particular direction are not drawn.
helpviewer_keywords: ["2117693b-8d7e-4cd9-dfee-29b015d206b8","D3D10_CULL_BACK","D3D10_CULL_FRONT","D3D10_CULL_MODE","D3D10_CULL_MODE enumeration [Direct3D 10]","D3D10_CULL_NONE","d3d10/D3D10_CULL_BACK","d3d10/D3D10_CULL_FRONT","d3d10/D3D10_CULL_MODE","d3d10/D3D10_CULL_NONE","direct3d10.d3d10_cull_mode"]
old-location: direct3d10\d3d10_cull_mode.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_cull_mode.htm
ms.date: 12/05/2018
ms.keywords: 2117693b-8d7e-4cd9-dfee-29b015d206b8, D3D10_CULL_BACK, D3D10_CULL_FRONT, D3D10_CULL_MODE, D3D10_CULL_MODE enumeration [Direct3D 10], D3D10_CULL_NONE, d3d10/D3D10_CULL_BACK, d3d10/D3D10_CULL_FRONT, d3d10/D3D10_CULL_MODE, d3d10/D3D10_CULL_NONE, direct3d10.d3d10_cull_mode
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
req.typenames: D3D10_CULL_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_CULL_MODE
 - d3d10/D3D10_CULL_MODE
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
 - D3D10_CULL_MODE
---

# D3D10_CULL_MODE enumeration


## -description

Indicates triangles facing a particular direction are not drawn.

## -enum-fields

### -field D3D10_CULL_NONE:1

Always draw all triangles.

### -field D3D10_CULL_FRONT:2

Do not draw triangles that are front-facing.

### -field D3D10_CULL_BACK:3

Do not draw triangles that are back-facing.

## -remarks

This enumeration is part of a rasterizer-state object description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">D3D10_RASTERIZER_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
