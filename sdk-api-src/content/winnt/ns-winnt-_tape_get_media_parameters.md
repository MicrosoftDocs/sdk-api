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

# _TAPE_GET_MEDIA_PARAMETERS structure


## -description


The 
<b>TAPE_GET_MEDIA_PARAMETERS</b> structure describes the tape in the tape drive. It is used by the <a href="https://msdn.microsoft.com/87e59e29-e174-4462-b692-512c3380eb4d">GetTapeParameters</a>
		 function.


## -struct-fields




### -field Capacity

Total number of bytes on the current tape partition.


### -field Remaining

Number of bytes between the current position and the end of the current tape partition.


### -field BlockSize

Number of bytes per block.


### -field PartitionCount

Number of partitions on the tape.


### -field WriteProtected

If this member is <b>TRUE</b>, the tape is write-protected. Otherwise, it is not.


## -remarks



The 
<a href="https://msdn.microsoft.com/87e59e29-e174-4462-b692-512c3380eb4d">GetTapeParameters</a> function fills the <b>Remaining</b> and <b>Capacity</b> members with estimates of the tape remaining in the current tape partition and the total capacity of the current tape partition.




## -see-also




<a href="https://msdn.microsoft.com/87e59e29-e174-4462-b692-512c3380eb4d">GetTapeParameters</a>
 

 

