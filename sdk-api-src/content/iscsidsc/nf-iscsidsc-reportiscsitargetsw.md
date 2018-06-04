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

# ReportIScsiTargetsW function


## -description


The <b>ReportIscsiTargets</b> function retrieves the list of targets that the iSCSI initiator service has discovered, and can also instruct the iSCSI initiator service to refresh the list.



## -parameters




### -param ForceUpdate [in]

If <b>true</b>, the iSCSI initiator service updates the list of discovered targets before returning the target list data to the caller.


### -param BufferSize [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 



### -param Buffer [out]

Pointer to a buffer that receives and contains the list of targets. The list consists of <b>null</b>-terminated strings. The last string, however, is double <b>null</b>-terminated.


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer size is insufficient to contain  the output data. Otherwise, <b>ReportIscsiTargets</b> returns the appropriate Win32 or iSCSI error code on failure.





## -see-also




<a href="https://msdn.microsoft.com/f082acc3-98d6-4758-aded-cb83e150e6d1">ReportIscsiSendTargetPortals</a>
 

 

