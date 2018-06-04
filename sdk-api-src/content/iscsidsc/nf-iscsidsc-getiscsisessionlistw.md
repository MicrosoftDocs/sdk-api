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

# GetIScsiSessionListW function


## -description


The <b>GetIscsiSessionList</b> function retrieves the list of active iSCSI sessions.



## -parameters




### -param BufferSize [in, out]

A pointer to a location that, on input, contains the size, in bytes, of the caller-allocated buffer that <i>SessionInfo</i> points to. If the operation succeeds, the location receives the size, in bytes, of the session information data that was retrieved. 

If the operation fails because the output buffer size was insufficient, the location receives the size, in bytes, of the buffer size required to contain the output data.


### -param SessionCount [out]

A pointer to a location that, on input, contains the number of <a href="https://msdn.microsoft.com/5da4aa28-a630-41f2-abb2-5538c11242e6">ISCSI_SESSION_INFO</a> structures that the buffer that <i>SessionInfo</i> points to can contain. If the operation succeeds, the location receives the number of <b>ISCSI_SESSION_INFO</b> structures that were retrieved.


### -param SessionInfo [out]

A pointer to a buffer that contains a series of contiguous structures of type <a href="https://msdn.microsoft.com/5da4aa28-a630-41f2-abb2-5538c11242e6">ISCSI_SESSION_INFO</a> that describe the active login sessions. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the size of the buffer at <i>SessionInfo</i> was insufficient to hold the output data. 

Otherwise, <b>GetIscsiSessionList</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/5da4aa28-a630-41f2-abb2-5538c11242e6">ISCSI_SESSION_INFO</a>
 

 

