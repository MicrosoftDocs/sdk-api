---
UID: NS:d3d12.D3D12_SUBRESOURCE_FOOTPRINT
title: D3D12_SUBRESOURCE_FOOTPRINT (d3d12.h)
description: Describes the format, width, height, depth, and row-pitch of the subresource into the parent resource.
helpviewer_keywords: ["D3D12_SUBRESOURCE_FOOTPRINT","D3D12_SUBRESOURCE_FOOTPRINT structure","d3d12/D3D12_SUBRESOURCE_FOOTPRINT","direct3d12.d3d12_subresource_footprint"]
old-location: direct3d12\d3d12_subresource_footprint.htm
tech.root: direct3d12
ms.assetid: C73B6AB0-F9C5-432E-BA26-3B7772411C95
ms.date: 12/05/2018
ms.keywords: D3D12_SUBRESOURCE_FOOTPRINT, D3D12_SUBRESOURCE_FOOTPRINT structure, d3d12/D3D12_SUBRESOURCE_FOOTPRINT, direct3d12.d3d12_subresource_footprint
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
req.typenames: D3D12_SUBRESOURCE_FOOTPRINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SUBRESOURCE_FOOTPRINT
 - d3d12/D3D12_SUBRESOURCE_FOOTPRINT
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
 - D3D12_SUBRESOURCE_FOOTPRINT
---

# D3D12_SUBRESOURCE_FOOTPRINT structure


## -description

Describes the format, width, height, depth, and row-pitch of the subresource into the parent resource.

## -struct-fields

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value that  specifies the viewing format.

### -field Width

The width of the subresource.

### -field Height

The height of the subresource.

### -field Depth

The depth of the subresource.

### -field RowPitch

The row pitch, or width, or physical size, in bytes, of the subresource data.
            This must be a multiple of D3D12_TEXTURE_DATA_PITCH_ALIGNMENT (256), and must be greater than or equal to the size of the data within a row.

## -remarks

Use this structure in the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structure.
      

The helper structure is <a href="/windows/desktop/direct3d12/cd3dx12-subresource-footprint">CD3DX12_SUBRESOURCE_FOOTPRINT</a>.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-subresource-footprint">CD3DX12_SUBRESOURCE_FOOTPRINT</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>