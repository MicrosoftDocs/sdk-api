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

# CREATE_USN_JOURNAL_DATA structure


## -description


Contains information that describes an update sequence number (USN) change journal.


## -struct-fields




### -field MaximumSize

The target maximum size that the NTFS file system allocates for the change journal, in bytes.

The change journal can grow larger than this value, but it is then truncated at the next NTFS file system 
       checkpoint to less than this value.


### -field AllocationDelta

The size of memory allocation that is added to the end and removed from the beginning of the change journal, in bytes.

The change journal can grow to more than the sum of the values of <b>MaximumSize</b> and 
       <b>AllocationDelta</b> before being trimmed.


## -remarks



For more information, see 
    <a href="https://msdn.microsoft.com/26cbacc2-d26b-434b-91b5-31aedc96da13">Creating, Modifying, and Deleting a Change Journal</a>.




## -see-also




<a href="https://msdn.microsoft.com/92e737e6-dba6-47f1-a077-e303039e12eb">FSCTL_CREATE_USN_JOURNAL</a>
 

 

