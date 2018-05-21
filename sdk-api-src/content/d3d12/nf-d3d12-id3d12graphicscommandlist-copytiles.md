---
UID: NF:d3d12.ID3D12GraphicsCommandList.CopyTiles
title: ID3D12GraphicsCommandList::CopyTiles
author: windows-driver-content
description: Copies tiles from buffer to tiled resource or vice versa.
old-location: direct3d12\id3d12graphicscommandlist_copytiles.htm
old-project: direct3d12
ms.assetid: F770CE6B-DD70-4102-BEFD-3E46B9957F5E
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: CopyTiles, CopyTiles method, CopyTiles method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,CopyTiles method, ID3D12GraphicsCommandList.CopyTiles, ID3D12GraphicsCommandList::CopyTiles, d3d12/ID3D12GraphicsCommandList::CopyTiles, direct3d12.id3d12graphicscommandlist_copytiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12GraphicsCommandList.CopyTiles
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::CopyTiles


## -description



        Copies tiles from buffer to tiled resource or vice versa.
      


## -parameters




### -param pTiledResource [in]

Type: <b>ID3D12Resource*</b>

A pointer to a tiled resource.


### -param pTileRegionStartCoordinate [in]

Type: <b>const <a href="https://msdn.microsoft.com/B7C51C7A-8500-4570-99C1-AE51D6A88529">D3D12_TILED_RESOURCE_COORDINATE</a>*</b>


            A pointer to a
            <a href="https://msdn.microsoft.com/B7C51C7A-8500-4570-99C1-AE51D6A88529">D3D12_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the tiled resource.
          


### -param pTileRegionSize [in]

Type: <b>const <a href="https://msdn.microsoft.com/6F71BD17-09B5-4638-9CD4-E2D3BBA97044">D3D12_TILE_REGION_SIZE</a>*</b>


            A pointer to a <a href="https://msdn.microsoft.com/6F71BD17-09B5-4638-9CD4-E2D3BBA97044">D3D12_TILE_REGION_SIZE</a> structure that describes the size of the tiled region.
          


### -param pBuffer [in]

Type: <b>ID3D12Resource*</b>


            A pointer to an <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> that represents a default, dynamic, or staging buffer.
          


### -param BufferStartOffsetInBytes

Type: <b>UINT64</b>


            The offset in bytes into the buffer at <i>pBuffer</i> to start the operation.
          


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/A540A369-DF23-4961-8213-B4B2B5C365E5">D3D12_TILE_COPY_FLAGS</a></b>


            A combination of <a href="https://msdn.microsoft.com/A540A369-DF23-4961-8213-B4B2B5C365E5">D3D12_TILE_COPY_FLAGS</a>-typed values that are combined by using a bitwise OR operation and that identifies how to copy tiles.
          


## -returns




            This method does not return a value.
          




## -remarks



<b>CopyTiles</b> drops write operations to 
		  unmapped areas and handles read operations from unmapped areas 
		  (except on Tier_1 tiled resources, 
		  where reading and writing unmapped areas is invalid - refer to <a href="https://msdn.microsoft.com/ADBA96C3-BD9E-4F12-89C8-371F6F7D369D">D3D12_TILED_RESOURCES_TIER</a>).
      

If a copy operation involves writing to the same memory location multiple times because multiple locations in the 
		destination resource are mapped to the same tile memory, the resulting write operations to multi-mapped tiles are 
		non-deterministic and non-repeatable; that is, accesses to the tile memory happen in whatever order the hardware 
		happens to execute the copy operation. 


        The tiles involved in the copy operation can't include tiles that contain packed mipmaps or results of the copy 
		  operation are undefined. To transfer data to and from mipmaps that the hardware packs into one tile, you must 
		  use the standard (that is, non-tile specific) copy APIs 
		  like <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>.

<b>CopyTiles</b> does copy data in a slightly different pattern than the standard copy methods.


        The memory layout of the tiles in the non-tiled buffer resource side of the copy operation is linear in memory within 64 KB tiles, which the hardware and driver swizzle and de-swizzle per tile as appropriate when they transfer to and from a tiled resource. For multisample antialiasing (MSAA) surfaces, the hardware and driver traverse each pixel's samples in sample-index order before they move to the next pixel. For tiles that are partially filled on the right side (for a surface that has a width not a multiple of tile width in pixels), the pitch and stride to move down a row is the full size in bytes of the number pixels that would fit across the tile if the tile was full. So, there can be a gap between each row of pixels in memory. Mipmaps that are smaller than a tile are not packed together in the linear layout, which might seem to be a waste of memory space, but as mentioned you can't use <b>CopyTiles</b> to copy to mipmaps that the hardware packs together. You can just use generic copy APIs, like <a href="https://msdn.microsoft.com/2EAFC6B9-376C-4801-8E53-BF0DB08943AA">CopyTextureRegion</a>, to copy small mipmaps individually.




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>



<a href="https://msdn.microsoft.com/03083460-192B-40CB-8EE1-76DF6D95F72B">Tiled resources</a>
 

 

