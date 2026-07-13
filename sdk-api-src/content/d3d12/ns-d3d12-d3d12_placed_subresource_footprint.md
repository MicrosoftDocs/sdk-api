---
UID: NS:d3d12.D3D12_PLACED_SUBRESOURCE_FOOTPRINT
title: D3D12_PLACED_SUBRESOURCE_FOOTPRINT (d3d12.h)
description: Describes the footprint of a placed subresource, including the offset and the D3D12_SUBRESOURCE_FOOTPRINT.
helpviewer_keywords: ["D3D12_PLACED_SUBRESOURCE_FOOTPRINT","D3D12_PLACED_SUBRESOURCE_FOOTPRINT structure","d3d12/D3D12_PLACED_SUBRESOURCE_FOOTPRINT","direct3d12.d3d12_placed_subresource_footprint"]
old-location: direct3d12\d3d12_placed_subresource_footprint.htm
tech.root: direct3d12
ms.assetid: 74740A52-C2A5-4AF6-92CC-85B5C214423F
ms.date: 12/05/2018
ms.keywords: D3D12_PLACED_SUBRESOURCE_FOOTPRINT, D3D12_PLACED_SUBRESOURCE_FOOTPRINT structure, d3d12/D3D12_PLACED_SUBRESOURCE_FOOTPRINT, direct3d12.d3d12_placed_subresource_footprint
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
req.typenames: D3D12_PLACED_SUBRESOURCE_FOOTPRINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_PLACED_SUBRESOURCE_FOOTPRINT
 - d3d12/D3D12_PLACED_SUBRESOURCE_FOOTPRINT
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
 - D3D12_PLACED_SUBRESOURCE_FOOTPRINT
---

# D3D12_PLACED_SUBRESOURCE_FOOTPRINT structure


## -description

Describes the footprint of a placed subresource, including the offset and the D3D12_SUBRESOURCE_FOOTPRINT.

## -struct-fields

### -field Offset

The offset of the subresource within the parent resource, in bytes.
            The offset between the start of the parent resource and this subresource. 
            
This value must be aligned to D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT (512) unless <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options13">D3D12_FEATURE_DATA_D3D12_OPTIONS13::UnrestrictedBufferTextureCopyPitchSupported</a> is TRUE.

### -field Footprint

The format, width, height, depth, and row-pitch of the subresource,
            as a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint">D3D12_SUBRESOURCE_FOOTPRINT</a> structure.

## -remarks

This structure is used in the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a> structure,
          and by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints">ID3D12Device::GetCopyableFootprints</a>.
        

All the data referenced by the footprint structure must fit within the bounds of the parent resource. If you use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints">GetCopyableFootprints</a> to fill out the structure, the <i>pTotalBytes</i> output field indicates the required size of the resource.

This structure is also used a number of helper functions (refer to <a href="/windows/desktop/direct3d12/helper-structures-and-functions-for-d3d12">Helper Structures and Functions for D3D12</a>).

When copying textures, use this structure along with <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
