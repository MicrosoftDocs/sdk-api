---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

