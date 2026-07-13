---
UID: NE:d3d11.D3D11_TILED_RESOURCES_TIER
title: D3D11_TILED_RESOURCES_TIER (d3d11.h)
description: Indicates the tier level at which tiled resources are supported.
helpviewer_keywords: ["D3D11_TILED_RESOURCES_NOT_SUPPORTED","D3D11_TILED_RESOURCES_TIER","D3D11_TILED_RESOURCES_TIER enumeration [Direct3D 11]","D3D11_TILED_RESOURCES_TIER_1","D3D11_TILED_RESOURCES_TIER_2","D3D11_TILED_RESOURCES_TIER_3","d3d11/D3D11_TILED_RESOURCES_NOT_SUPPORTED","d3d11/D3D11_TILED_RESOURCES_TIER","d3d11/D3D11_TILED_RESOURCES_TIER_1","d3d11/D3D11_TILED_RESOURCES_TIER_2","d3d11/D3D11_TILED_RESOURCES_TIER_3","direct3d11.d3d11_tiled_resources_tier"]
old-location: direct3d11\d3d11_tiled_resources_tier.htm
tech.root: direct3d11
ms.assetid: F2E58CDC-4E65-4166-976A-E58B6DC7B1E8
ms.date: 12/05/2018
ms.keywords: D3D11_TILED_RESOURCES_NOT_SUPPORTED, D3D11_TILED_RESOURCES_TIER, D3D11_TILED_RESOURCES_TIER enumeration [Direct3D 11], D3D11_TILED_RESOURCES_TIER_1, D3D11_TILED_RESOURCES_TIER_2, D3D11_TILED_RESOURCES_TIER_3, d3d11/D3D11_TILED_RESOURCES_NOT_SUPPORTED, d3d11/D3D11_TILED_RESOURCES_TIER, d3d11/D3D11_TILED_RESOURCES_TIER_1, d3d11/D3D11_TILED_RESOURCES_TIER_2, d3d11/D3D11_TILED_RESOURCES_TIER_3, direct3d11.d3d11_tiled_resources_tier
req.header: d3d11.h
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
req.typenames: D3D11_TILED_RESOURCES_TIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TILED_RESOURCES_TIER
 - d3d11/D3D11_TILED_RESOURCES_TIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TILED_RESOURCES_TIER
---

# D3D11_TILED_RESOURCES_TIER enumeration


## -description

Indicates the tier level at which tiled resources are supported.

## -enum-fields

### -field D3D11_TILED_RESOURCES_NOT_SUPPORTED:0

Tiled resources are not supported.

### -field D3D11_TILED_RESOURCES_TIER_1:1

Tier_1 tiled resources are supported.

The device supports calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">CreateTexture2D</a> and so on with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_TILED</a> flag.
            

The device supports calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createbuffer">CreateBuffer</a> with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_TILE_POOL</a> flag.
            

If you access tiles (read or write) that are <b>NULL</b>-mapped, you get undefined behavior, which includes device-removed.  Apps can map all tiles to a single "default" tile to avoid this condition.

### -field D3D11_TILED_RESOURCES_TIER_2:2

Tier_2 tiled resources are supported.
            

Superset of Tier_1 functionality, which includes this additional support:
              

<ul>
<li>On Tier_1, if the size of a texture mipmap level is an integer multiple of the standard tile shape for its format, it is guaranteed to be nonpacked. On Tier_2, this guarantee is expanded to include mipmap levels whose size is at least one standard tile shape.
                For more info, see <a href="/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc">D3D11_PACKED_MIP_DESC</a>.
              </li>
<li>Shader instructions are available for clamping level-of-detail (LOD) and for obtaining status about the shader operation. For info about one of these shader instructions, see <a href="/windows/desktop/direct3dhlsl/sample-s-float--int-uint-">Sample(S,float,int,float,uint)</a>.
              </li>
<li>Reading from <b>NULL</b>-mapped tiles treat that sampled value as zero.  Writes to <b>NULL</b>-mapped tiles are discarded.
              </li>
</ul>

### -field D3D11_TILED_RESOURCES_TIER_3:3

Tier_3 tiled resources are supported.
            

Superset of Tier_2 functionality, Tier 3 is essentially Tier 2 but with the additional support of Texture3D for Tiled Resources.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>



<a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options1">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a>
