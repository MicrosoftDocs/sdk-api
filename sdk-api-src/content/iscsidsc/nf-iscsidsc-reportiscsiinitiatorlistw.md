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

# ReportIScsiInitiatorListW function


## -description


The <b>ReportIscsiInitiatorList</b> function retrieves the list of initiator Host Bus Adapters that are running on the machine.



## -parameters




### -param BufferSize [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 
If the operation succeeds, this location receives the size, represented by a number of elements, that corresponds to the retreived data.


### -param Buffer [out]

A buffer that, on output, is filled with the list of initiator names. Each initiator name is a <b>null</b>-terminated string, except for the last initiator name, which is double-<b>null</b> terminated.


## -returns



 Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer size of Buffer is insufficient to contain the output data.

 Otherwise, <b>ReportIscsiInitiatorList</b> returns the appropriate Win32 or iSCSI error code on failure.



