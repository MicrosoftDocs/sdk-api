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

# _CLS_ARCHIVE_DESCRIPTOR structure


## -description


Used by the <a href="https://msdn.microsoft.com/4aaf10bd-e9df-435b-a756-5ae5c1eb2903">GetNextLogArchiveExtent</a> function to return information about log archive extents.


## -struct-fields




### -field coffLow

The offset in the container  to the first byte of the archive extent.


### -field coffHigh

The offset in the container to the last byte of the archive extent.


### -field infoContainer

The container information structure  that describes the container associated with the archive extent. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541782">CLFS_CONTAINER_INFORMATION</a>.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541782">CLFS_CONTAINER_INFORMATION</a>



<a href="https://msdn.microsoft.com/4aaf10bd-e9df-435b-a756-5ae5c1eb2903">GetNextLogArchiveExtent</a>
 

 

