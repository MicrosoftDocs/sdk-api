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
 

 

