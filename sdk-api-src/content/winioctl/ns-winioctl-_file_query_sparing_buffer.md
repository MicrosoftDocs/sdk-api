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

# _FILE_QUERY_SPARING_BUFFER structure


## -description


Contains   defect management properties.


## -struct-fields




### -field SparingUnitBytes

The size of a sparing packet and the underlying error check and correction (ECC) block size of the volume.


### -field SoftwareSparing

If <b>TRUE</b>, indicates that sparing behavior is software-based; if <b>FALSE</b>, it is hardware-based.


### -field TotalSpareBlocks

The total number of blocks allocated for sparing.


### -field FreeSpareBlocks

The  number of blocks available for sparing.


## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/72122388-a42f-4c67-9539-20eb4c59dcf0">FSCTL_QUERY_SPARING_INFO</a>
 

 

