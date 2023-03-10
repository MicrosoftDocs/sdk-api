---
UID: NS:d3d12.D3D12_SUBRESOURCE_TILING
title: D3D12_SUBRESOURCE_TILING (d3d12.h)
description: Describes a tiled subresource volume. (D3D12_SUBRESOURCE_TILING)
helpviewer_keywords: ["D3D12_SUBRESOURCE_TILING","D3D12_SUBRESOURCE_TILING structure","d3d12/D3D12_SUBRESOURCE_TILING","direct3d12.d3d12_subresource_tiling"]
old-location: direct3d12\d3d12_subresource_tiling.htm
tech.root: direct3d12
ms.assetid: 81C93E0F-AF05-4801-97EB-6C3E0407B5F6
ms.date: 12/05/2018
ms.keywords: D3D12_SUBRESOURCE_TILING, D3D12_SUBRESOURCE_TILING structure, d3d12/D3D12_SUBRESOURCE_TILING, direct3d12.d3d12_subresource_tiling
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
req.typenames: D3D12_SUBRESOURCE_TILING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SUBRESOURCE_TILING
 - d3d12/D3D12_SUBRESOURCE_TILING
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
 - D3D12_SUBRESOURCE_TILING
---

# D3D12_SUBRESOURCE_TILING structure


## -description

Describes a tiled subresource volume.

## -struct-fields

### -field WidthInTiles

The width in tiles of the subresource.

### -field HeightInTiles

The height in tiles of the subresource.

### -field DepthInTiles

The depth in tiles of the subresource.

### -field StartTileIndexInOverallResource

The index of the tile in the overall tiled subresource to start with.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling">GetResourceTiling</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-subresource-tiling">CD3DX12_SUBRESOURCE_TILING</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
