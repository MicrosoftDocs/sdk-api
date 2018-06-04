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

# GetIScsiInitiatorNodeNameA function


## -description


The <b>GetIscsiInitiatorNodeName</b> function retrieves the common initiator node name that is used when establishing sessions from the local machine.


## -parameters




### -param InitiatorNodeName

A caller-allocated buffer that, on output, receives the node name. The buffer must be large enough to hold <b>MAX_ISCSI_NAME_LEN+1</b> bytes. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and the appropriate Win32 or iSCSI error code if the operation fails.





## -remarks



All initiator Host Bus Adapters, both software and hardware, use the same node name when establishing sessions.



