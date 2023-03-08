---
UID: NS:d3d12.D3D12_TILED_RESOURCE_COORDINATE
title: D3D12_TILED_RESOURCE_COORDINATE (d3d12.h)
description: Describes the coordinates of a tiled resource. (D3D12_TILED_RESOURCE_COORDINATE)
helpviewer_keywords: ["D3D12_TILED_RESOURCE_COORDINATE","D3D12_TILED_RESOURCE_COORDINATE structure","d3d12/D3D12_TILED_RESOURCE_COORDINATE","direct3d12.d3d12_tiled_resource_coordinate"]
old-location: direct3d12\d3d12_tiled_resource_coordinate.htm
tech.root: direct3d12
ms.assetid: B7C51C7A-8500-4570-99C1-AE51D6A88529
ms.date: 12/05/2018
ms.keywords: D3D12_TILED_RESOURCE_COORDINATE, D3D12_TILED_RESOURCE_COORDINATE structure, d3d12/D3D12_TILED_RESOURCE_COORDINATE, direct3d12.d3d12_tiled_resource_coordinate
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
req.typenames: D3D12_TILED_RESOURCE_COORDINATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TILED_RESOURCE_COORDINATE
 - d3d12/D3D12_TILED_RESOURCE_COORDINATE
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
 - D3D12_TILED_RESOURCE_COORDINATE
---

# D3D12_TILED_RESOURCE_COORDINATE structure


## -description

Describes the coordinates of a tiled resource.

## -struct-fields

### -field X

The x-coordinate of the tiled resource.

### -field Y

The y-coordinate of the tiled resource.

### -field Z

The z-coordinate of the tiled resource.

### -field Subresource

The index of the subresource for the tiled resource.

For mipmaps that use nonstandard tiling, or are packed, or both use nonstandard tiling and are packed, any subresource value that indicates any of the packed mipmaps all refer to the same tile. Additionally, the X coordinate is used to indicate a tile within the packed mip region, rather than a logical region of a single subresource. The Y and Z coordinates must be zero.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">CopyTiles</a>, <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a> methods.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-tiled-resource-coordinate">CD3DX12_TILED_RESOURCE_COORDINATE</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
