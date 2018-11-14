---
UID: NE:d3d12.D3D12_TILE_RANGE_FLAGS
title: D3D12_TILE_RANGE_FLAGS
author: windows-sdk-content
description: Specifies a range of tile mappings.
old-location: direct3d12\d3d12_tile_range_flags.htm
tech.root: direct3d12
ms.assetid: D6C35804-4F83-4F33-A4A3-06C5D73174FB
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_TILE_RANGE_FLAGS, D3D12_TILE_RANGE_FLAGS enumeration, D3D12_TILE_RANGE_FLAG_NONE, D3D12_TILE_RANGE_FLAG_NULL, D3D12_TILE_RANGE_FLAG_REUSE_SINGLE_TILE, D3D12_TILE_RANGE_FLAG_SKIP, d3d12/D3D12_TILE_RANGE_FLAGS, d3d12/D3D12_TILE_RANGE_FLAG_NONE, d3d12/D3D12_TILE_RANGE_FLAG_NULL, d3d12/D3D12_TILE_RANGE_FLAG_REUSE_SINGLE_TILE, d3d12/D3D12_TILE_RANGE_FLAG_SKIP, direct3d12.d3d12_tile_range_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - D3D12_TILE_RANGE_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_TILE_RANGE_FLAGS
req.redist: 
---

# D3D12_TILE_RANGE_FLAGS enumeration


## -description


Specifies a range of tile mappings.
        


## -enum-fields




### -field D3D12_TILE_RANGE_FLAG_NONE

No tile-mapping flags are specified.
          


### -field D3D12_TILE_RANGE_FLAG_NULL

The tile range is <b>NULL</b>.
          


### -field D3D12_TILE_RANGE_FLAG_SKIP

Skip the tile range.
          


### -field D3D12_TILE_RANGE_FLAG_REUSE_SINGLE_TILE

Reuse a single tile in the tile range.
          


## -remarks



Use these flags with <a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">ID3D12CommandQueue::UpdateTileMappings</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

