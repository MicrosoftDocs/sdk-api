---
UID: NF:d3d12.ID3D12CommandQueue.CopyTileMappings
title: ID3D12CommandQueue::CopyTileMappings (d3d12.h)
description: Copies mappings from a source reserved resource to a destination reserved resource.
helpviewer_keywords: ["CopyTileMappings","CopyTileMappings method","CopyTileMappings method","ID3D12CommandQueue interface","ID3D12CommandQueue interface","CopyTileMappings method","ID3D12CommandQueue.CopyTileMappings","ID3D12CommandQueue::CopyTileMappings","d3d12/ID3D12CommandQueue::CopyTileMappings","direct3d12.id3d12commandqueue_copytilemappings"]
old-location: direct3d12\id3d12commandqueue_copytilemappings.htm
tech.root: direct3d12
ms.assetid: FAFA4B5C-EA3C-4209-AB8E-75F3B90F3745
ms.date: 12/05/2018
ms.keywords: CopyTileMappings, CopyTileMappings method, CopyTileMappings method,ID3D12CommandQueue interface, ID3D12CommandQueue interface,CopyTileMappings method, ID3D12CommandQueue.CopyTileMappings, ID3D12CommandQueue::CopyTileMappings, d3d12/ID3D12CommandQueue::CopyTileMappings, direct3d12.id3d12commandqueue_copytilemappings
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12CommandQueue::CopyTileMappings
 - d3d12/ID3D12CommandQueue::CopyTileMappings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12CommandQueue.CopyTileMappings
---

# ID3D12CommandQueue::CopyTileMappings


## -description

Copies mappings from a source reserved resource to a destination reserved resource.

## -parameters

### -param pDstResource [in]

A pointer to the destination reserved resource.

### -param pDstRegionStartCoordinate [in]

A pointer to a
            <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the destination reserved resource.

### -param pSrcResource [in]

A pointer to the source reserved resource.

### -param pSrcRegionStartCoordinate [in]

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate">D3D12_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the source reserved resource.

### -param pRegionSize [in]

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size">D3D12_TILE_REGION_SIZE</a> structure that describes the size of the reserved region.

### -param Flags

One member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags">D3D12_TILE_MAPPING_FLAGS</a>.

## -remarks

Use <b>CopyTileMappings</b> to copy the tile mappings from one reserved resource to another, either to duplicate a resource mapping, or to initialize a new mapping before modifying it using <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a>.

<b>CopyTileMappings</b> helps with tasks such as shifting mappings around within and across reserved resources, for example, scrolling tiles. 
        The source and destination regions can overlap; the result of the copy in this situation is as if the source was saved to a temporary location 
        and from there written to the destination.
      

The destination and the source regions must each entirely fit in their resource or behavior is undefined and the debug layer will emit an error.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue">ID3D12CommandQueue</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a>



<a href="/windows/desktop/direct3d12/volume-tiled-resources">Volume Tiled Resources</a>