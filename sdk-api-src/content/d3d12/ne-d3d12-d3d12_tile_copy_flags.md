---
UID: NE:d3d12.D3D12_TILE_COPY_FLAGS
title: D3D12_TILE_COPY_FLAGS
author: windows-sdk-content
description: Specifies how to copy a tile.
old-location: direct3d12\d3d12_tile_copy_flags.htm
tech.root: direct3d12
ms.assetid: A540A369-DF23-4961-8213-B4B2B5C365E5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: D3D12_TILE_COPY_FLAGS, D3D12_TILE_COPY_FLAGS enumeration, D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE, D3D12_TILE_COPY_FLAG_NONE, D3D12_TILE_COPY_FLAG_NO_HAZARD, D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER, d3d12/D3D12_TILE_COPY_FLAGS, d3d12/D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE, d3d12/D3D12_TILE_COPY_FLAG_NONE, d3d12/D3D12_TILE_COPY_FLAG_NO_HAZARD, d3d12/D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER, direct3d12.d3d12_tile_copy_flags
ms.prod: windows
ms.technology: windows-sdk
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
 - d3d12.h
api_name:
 - D3D12_TILE_COPY_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_TILE_COPY_FLAGS
req.redist: 
---

# D3D12_TILE_COPY_FLAGS enumeration


## -description


Specifies how to copy a tile.
        


## -enum-fields




### -field D3D12_TILE_COPY_FLAG_NONE

No tile-copy flags are specified.
          


### -field D3D12_TILE_COPY_FLAG_NO_HAZARD

Indicates that the GPU isn't currently referencing any of the
            portions of destination memory being written.
          


### -field D3D12_TILE_COPY_FLAG_LINEAR_BUFFER_TO_SWIZZLED_TILED_RESOURCE

Indicates that the <a href="https://msdn.microsoft.com/F770CE6B-DD70-4102-BEFD-3E46B9957F5E">ID3D12GraphicsCommandList::CopyTiles</a> operation involves copying a linear buffer to a swizzled tiled resource. This means to copy tile data from the
            specified buffer location, reading tiles sequentially,
            to the specified tile region (in x,y,z order if the region is a box), swizzling to optimal hardware memory layout as needed.
            In this <b>ID3D12GraphicsCommandList::CopyTiles</b> call, you specify the source data with the  <i>pBuffer</i> parameter and the destination with the <i>pTiledResource</i> parameter.
          


### -field D3D12_TILE_COPY_FLAG_SWIZZLED_TILED_RESOURCE_TO_LINEAR_BUFFER

Indicates that the <a href="https://msdn.microsoft.com/F770CE6B-DD70-4102-BEFD-3E46B9957F5E">ID3D12GraphicsCommandList::CopyTiles</a> operation involves copying a swizzled tiled resource to a linear buffer. This means to copy tile data from the tile region, reading tiles sequentially (in x,y,z order if the region is a box),
            to the specified buffer location, deswizzling to linear memory layout as needed.
            In this <b>ID3D12GraphicsCommandList::CopyTiles</b> call, you specify the source data with the <i>pTiledResource</i> parameter and the destination with the  <i>pBuffer</i> parameter.
          


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/F770CE6B-DD70-4102-BEFD-3E46B9957F5E">CopyTiles</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

