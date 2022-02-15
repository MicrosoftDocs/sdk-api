---
UID: NE:d3d10.D3D10_MAP_FLAG
title: D3D10_MAP_FLAG (d3d10.h)
description: Specifies how the CPU should respond when Map is called on a resource being used by the GPU.
helpviewer_keywords: ["D3D10_MAP_FLAG","D3D10_MAP_FLAG enumeration [Direct3D 10]","D3D10_MAP_FLAG_DO_NOT_WAIT","b065a6b9-984f-67e0-f7d5-c91d03926340","d3d10/D3D10_MAP_FLAG","d3d10/D3D10_MAP_FLAG_DO_NOT_WAIT","direct3d10.d3d10_map_flag"]
old-location: direct3d10\d3d10_map_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_map_flag.htm
ms.date: 12/05/2018
ms.keywords: D3D10_MAP_FLAG, D3D10_MAP_FLAG enumeration [Direct3D 10], D3D10_MAP_FLAG_DO_NOT_WAIT, b065a6b9-984f-67e0-f7d5-c91d03926340, d3d10/D3D10_MAP_FLAG, d3d10/D3D10_MAP_FLAG_DO_NOT_WAIT, direct3d10.d3d10_map_flag
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
req.typenames: D3D10_MAP_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_MAP_FLAG
 - d3d10/D3D10_MAP_FLAG
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
 - D3D10_MAP_FLAG
---

# D3D10_MAP_FLAG enumeration


## -description

Specifies how the CPU should respond when Map is called on a resource being used by the GPU.

## -enum-fields

### -field D3D10_MAP_FLAG_DO_NOT_WAIT:0x100000L

Specifies that Map should return <b>DXGI_ERROR_WAS_STILL_DRAWING</b> when the GPU blocks the CPU from accessing a resource.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10buffer-map">ID3D10Buffer::Map</a>, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10texture1d-map">ID3D10Texture1D::Map</a>, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10texture2d-map">ID3D10Texture2D::Map</a>, and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10texture3d-map">ID3D10Texture3D::Map</a>.

D3D10_MAP_FLAG_DO_NOT_WAIT cannot be used with <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP_WRITE_DISCARD</a> or <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_map">D3D10_MAP_WRITE_NOOVERWRITE</a>.

For more information about potential conflicts between the GPU and CPU during resource mapping, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">Copying and Accessing Resource Data (Direct3D 10)</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-enums">Resource Enumerations</a>
