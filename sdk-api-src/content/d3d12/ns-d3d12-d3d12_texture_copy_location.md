---
UID: NS:d3d12.D3D12_TEXTURE_COPY_LOCATION
title: D3D12_TEXTURE_COPY_LOCATION (d3d12.h)
description: Describes a portion of a texture for the purpose of texture copies.
helpviewer_keywords: ["D3D12_TEXTURE_COPY_LOCATION","D3D12_TEXTURE_COPY_LOCATION structure","d3d12/D3D12_TEXTURE_COPY_LOCATION","direct3d12.d3d12_texture_copy_location"]
old-location: direct3d12\d3d12_texture_copy_location.htm
tech.root: direct3d12
ms.assetid: D63EC731-EE75-44CD-9CCD-7FB4A761D1A3
ms.date: 12/05/2018
ms.keywords: D3D12_TEXTURE_COPY_LOCATION, D3D12_TEXTURE_COPY_LOCATION structure, d3d12/D3D12_TEXTURE_COPY_LOCATION, direct3d12.d3d12_texture_copy_location
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
req.typenames: D3D12_TEXTURE_COPY_LOCATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEXTURE_COPY_LOCATION
 - d3d12/D3D12_TEXTURE_COPY_LOCATION
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
 - D3D12_TEXTURE_COPY_LOCATION
---

# D3D12_TEXTURE_COPY_LOCATION structure


## -description

Describes a portion of a texture for the purpose of texture copies.

## -struct-fields

### -field pResource

Specifies the resource which will be used for the copy operation.<div> </div>When <b>Type</b> is D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT, <b>pResource</b> must point to a buffer resource.<div> </div>When <b>Type</b> is D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX, <b>pResource</b> must point to a texture resource.

### -field Type

Specifies which type of resource location this is: a subresource of a texture, or a description of a texture layout which can be applied to a buffer.
            This <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type">D3D12_TEXTURE_COPY_TYPE</a> enum indicates which union member to use.

### -field PlacedFootprint

Specifies a texture layout, with offset, dimensions, and pitches, for the hardware to understand how to treat a section of a buffer resource as a multi-dimensional texture.
              To fill-in the correct data for a <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a> call, 
              see <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>.

### -field SubresourceIndex

Specifies the index of the subresource of an arrayed, mip-mapped, or planar texture should be used for the copy operation.

## -remarks

Use this structure with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-texture-copy-location">CD3DX12_TEXTURE_COPY_LOCATION</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>