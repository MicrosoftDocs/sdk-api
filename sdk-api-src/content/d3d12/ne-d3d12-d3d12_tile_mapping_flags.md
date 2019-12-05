---
UID: NE:d3d12.D3D12_TILE_MAPPING_FLAGS
title: D3D12_TILE_MAPPING_FLAGS (d3d12.h)
description: Specifies how to perform a tile-mapping operation.
old-location: direct3d12\d3d12_tile_mapping_flags.htm
tech.root: direct3d12
ms.assetid: 588BCCA8-3F14-4837-86AE-EE4E4F0BC5ED
ms.date: 12/05/2018
ms.keywords: D3D12_TILE_MAPPING_FLAGS, D3D12_TILE_MAPPING_FLAGS enumeration, D3D12_TILE_MAPPING_FLAG_NONE, D3D12_TILE_MAPPING_FLAG_NO_HAZARD, d3d12/D3D12_TILE_MAPPING_FLAGS, d3d12/D3D12_TILE_MAPPING_FLAG_NONE, d3d12/D3D12_TILE_MAPPING_FLAG_NO_HAZARD, direct3d12.d3d12_tile_mapping_flags
ms.topic: enum
f1_keywords:
- d3d12/D3D12_TILE_MAPPING_FLAGS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D12.h
api_name:
- D3D12_TILE_MAPPING_FLAGS
targetos: Windows
req.typenames: D3D12_TILE_MAPPING_FLAGS
req.redist: 
ms.custom: 19H1
---

# D3D12_TILE_MAPPING_FLAGS enumeration


## -description


Specifies how to perform a tile-mapping operation.
        


## -enum-fields




### -field D3D12_TILE_MAPPING_FLAG_NONE

No tile-mapping flags are specified.
          


### -field D3D12_TILE_MAPPING_FLAG_NO_HAZARD

Unsupported, do not use.
			 


## -remarks



This enum is used by the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

