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

# ID3D12CommandQueue::CopyTileMappings


## -description


Copies mappings from a source reserved resource to a destination reserved resource.


## -parameters




### -param pDstResource [in]

A pointer to the destination reserved resource.


### -param pDstRegionStartCoordinate [in]


            A pointer to a
            <a href="https://msdn.microsoft.com/B7C51C7A-8500-4570-99C1-AE51D6A88529">D3D12_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the destination reserved resource.
          


### -param pSrcResource [in]

A pointer to the source reserved resource.


### -param pSrcRegionStartCoordinate [in]


            A pointer to a <a href="https://msdn.microsoft.com/B7C51C7A-8500-4570-99C1-AE51D6A88529">D3D12_TILED_RESOURCE_COORDINATE</a> structure that describes the starting coordinates of the source reserved resource.
          


### -param pRegionSize [in]


            A pointer to a <a href="https://msdn.microsoft.com/6F71BD17-09B5-4638-9CD4-E2D3BBA97044">D3D12_TILE_REGION_SIZE</a> structure that describes the size of the reserved region.
          


### -param Flags


            One member of <a href="https://msdn.microsoft.com/588BCCA8-3F14-4837-86AE-EE4E4F0BC5ED">D3D12_TILE_MAPPING_FLAGS</a>. 


## -returns



This method does not return a value. If an E_OUTOFMEMORY occurs, the device is removed.




## -remarks



Use <b>CopyTileMappings</b> to copy the tile mappings from one reserved resource to another, either to duplicate a resource mapping, or to initialize a new mapping before modifying it using <a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">UpdateTileMappings</a>.

<b>CopyTileMappings</b> helps with tasks such as shifting mappings around within and across reserved resources, for example, scrolling tiles. 
        The source and destination regions can overlap; the result of the copy in this situation is as if the source was saved to a temporary location 
        and from there written to the destination.
      

The destination and the source regions must each entirely fit in their resource or behavior is undefined and the debug layer will emit an error.


        For more info on tiled resources, refer to the  "DirectX tiled resources" section within <a href="http://msdn.microsoft.com/en-us/library/windows/apps/bg182880.aspx">DirectX programming</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>



<a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">UpdateTileMappings</a>



<a href="https://msdn.microsoft.com/F670D15D-BC0F-4F90-99C1-A35192FE8980">Volume Tiled Resources</a>
 

 

