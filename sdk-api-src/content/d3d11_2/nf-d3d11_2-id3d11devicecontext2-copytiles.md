---
UID: NF:d3d11_2.ID3D11DeviceContext2.CopyTiles
title: ID3D11DeviceContext2::CopyTiles
author: windows-sdk-content
description: Copies tiles from buffer to tiled resource or vice versa.
old-location: direct3d11\id3d11devicecontext2_copytiles.htm
tech.root: direct3d11
ms.assetid: C336B0C7-DB99-466C-B689-5D6634EE0B36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyTiles, CopyTiles method [Direct3D 11], CopyTiles method [Direct3D 11],ID3D11DeviceContext2 interface, ID3D11DeviceContext2 interface [Direct3D 11],CopyTiles method, ID3D11DeviceContext2.CopyTiles, ID3D11DeviceContext2::CopyTiles, d3d11_2/ID3D11DeviceContext2::CopyTiles, direct3d11.id3d11devicecontext2_copytiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext2.CopyTiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext2::CopyTiles


## -description


Copies tiles from buffer to tiled resource or vice versa. 


## -parameters




### -param pTiledResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to a tiled resource.


### -param pTileRegionStartCoordinate [in]

Type: <b>const <a href="https://msdn.microsoft.com/4639E5FA-44D7-4F6E-8843-17EE862BD9C4">D3D11_TILED_RESOURCE_COORDINATE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/4639E5FA-44D7-4F6E-8843-17EE862BD9C4">D3D11_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the tiled resource.
          


### -param pTileRegionSize [in]

Type: <b>const <a href="https://msdn.microsoft.com/D4A93462-9A2F-416A-9CC1-AC24DFF35890">D3D11_TILE_REGION_SIZE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/D4A93462-9A2F-416A-9CC1-AC24DFF35890">D3D11_TILE_REGION_SIZE</a> structure that describes the size of the tiled region.
          


### -param pBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a> that represents a default, dynamic, or staging buffer.
          


### -param BufferStartOffsetInBytes [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The offset in bytes into the buffer at <i>pBuffer</i> to start the operation.
          


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/1ACBABF2-A0C5-419B-9723-BD0FEEEDF478">D3D11_TILE_COPY_FLAG</a>-typed values that are combined by using a bitwise OR operation and that identifies how to copy tiles.
          


## -returns



Returns nothing




## -remarks



<b>CopyTiles</b> drops write operations to unmapped areas and handles read operations from unmapped areas (except on <a href="https://msdn.microsoft.com/F2E58CDC-4E65-4166-976A-E58B6DC7B1E8">Tier_1</a> tiled resources, where reading and writing unmapped areas is invalid).
      

If a copy operation involves writing to the same memory location multiple times because multiple locations in the destination resource are mapped to the same tile memory, the resulting write operations to multi-mapped tiles are non-deterministic and non-repeatable; that is, accesses to the tile memory happen in whatever order the hardware happens to execute the copy operation.

The tiles involved in the copy operation can't include tiles that contain packed mipmaps or results of the copy operation are undefined. To transfer data to and from mipmaps that the hardware packs into one tile, you must use the standard (that is, non-tile specific) copy and update APIs (like <a href="https://msdn.microsoft.com/1963011F-C3E2-428D-B667-195A4976510B">ID3D11DeviceContext1::CopySubresourceRegion1</a> and <a href="https://msdn.microsoft.com/7D89591C-F3F7-4A4F-A91A-AC67D9A573AF">ID3D11DeviceContext1::UpdateSubresource1</a>) or <a href="https://msdn.microsoft.com/43012c58-3b1a-4956-993f-4ff3f5ec7fce">ID3D11DeviceContext::GenerateMips</a> for the whole mipmap chain.
      

The memory layout of the tiles in the non-tiled buffer resource side of the copy operation is linear in memory within 64 KB tiles, which the hardware and driver swizzle and deswizzle per tile as appropriate when they transfer to and from a tiled resource. For multisample antialiasing (MSAA) surfaces, the hardware and driver traverse each pixel's samples in sample-index order before they move to the next pixel. For tiles that are partially filled on the right side (for a surface that has a width not a multiple of tile width in pixels), the pitch and stride to move down a row is the full size in bytes of the number pixels that would fit across the tile if the tile was full. So, there can be a gap between each row of pixels in memory. Mipmaps that are smaller than a tile are not packed together in the linear layout, which might seem to be a waste of memory space, but as mentioned you can't use <b>CopyTiles</b> or <a href="https://msdn.microsoft.com/EB0F9CBD-29B2-484D-8923-6686C73487F7">ID3D11DeviceContext2::UpdateTiles</a> to copy to mipmaps that the hardware packs together. You can just use generic copy and update APIs (like <a href="https://msdn.microsoft.com/1963011F-C3E2-428D-B667-195A4976510B">ID3D11DeviceContext1::CopySubresourceRegion1</a> and <a href="https://msdn.microsoft.com/7D89591C-F3F7-4A4F-A91A-AC67D9A573AF">ID3D11DeviceContext1::UpdateSubresource1</a>) to copy small mipmaps individually. Although in the case of a generic copy API (like <b>ID3D11DeviceContext1::CopySubresourceRegion1</b>), the linear memory must be the same dimension as the tiled resource; <b>ID3D11DeviceContext1::CopySubresourceRegion1</b> can't copy from a buffer resource to a Texture2D for instance.
      

For more info about tiled resources, see <a href="https://msdn.microsoft.com/03083460-192B-40CB-8EE1-76DF6D95F72B">Tiled resources</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

