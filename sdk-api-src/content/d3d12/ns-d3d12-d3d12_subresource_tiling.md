---
UID: NS:d3d12.D3D12_SUBRESOURCE_TILING
title: D3D12_SUBRESOURCE_TILING
author: windows-sdk-content
description: Describes a tiled subresource volume.
old-location: direct3d12\d3d12_subresource_tiling.htm
old-project: direct3d12
ms.assetid: 81C93E0F-AF05-4801-97EB-6C3E0407B5F6
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D12_SUBRESOURCE_TILING, D3D12_SUBRESOURCE_TILING structure, d3d12/D3D12_SUBRESOURCE_TILING, direct3d12.d3d12_subresource_tiling
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D12_SUBRESOURCE_TILING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_SUBRESOURCE_TILING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



This structure is used by the <a href="https://msdn.microsoft.com/32574750-92D3-4CAF-90C6-BA0DEF1E5464">GetResourceTiling</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/102E5E25-300B-40F2-A953-E40AD7EE61AD">CD3DX12_SUBRESOURCE_TILING</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

