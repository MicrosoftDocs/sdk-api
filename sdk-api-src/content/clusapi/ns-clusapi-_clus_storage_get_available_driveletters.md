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

# _CLUS_STORAGE_GET_AVAILABLE_DRIVELETTERS structure


## -description


Contains a bitmask of the driver letters that are available on  a node. It is used as the return value of the <a href="https://msdn.microsoft.com/7960baea-64b5-481b-9237-044ffa7b3b0a">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS</a> control code.


## -struct-fields




### -field AvailDrivelettersMask

The least significant bit represents the letter 'A' and is set to zero if any partition on the node has that drive letter in use. This convention continues until bit 26, which represents the letter 'Z'. The value of bits 27 through 32 is not defined.


## -see-also




<a href="https://msdn.microsoft.com/7960baea-64b5-481b-9237-044ffa7b3b0a">CLUSCTL_RESOURCE_TYPE_STORAGE_GET_DRIVELETTERS</a>
 

 

