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

# ReportActiveIScsiTargetMappingsW function


## -description


<b>ReportActiveIscsiTargetMappings</b> function retrieves the target mappings that are currently active for all initiators on the computer.


## -parameters




### -param BufferSize [in, out]

A pointer to a location that, on input, contains the size, in bytes, of the buffer that <i>Mappings</i> points to. If the operation succeeds, the location receives the size, in bytes, of the mapping data that was retrieved. If the buffer  that <i>Mappings</i> points to is not sufficient to contain the output data, the location receives the buffer size, in bytes, that is required. 


### -param MappingCount [out]

If the operation succeeds, the location pointed to by <i>MappingCount</i> receives the number of mappings that were retrieved.


### -param Mappings [out]

A pointer to an array of type <a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a> that, on output, is filled with the active target mappings for all initiators.


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer is not large enough.

Otherwise, <b>ReportActiveIscsiTargetMappings</b> returns the appropriate Win32 or iSCSI error code on failure.




## -remarks



Target mappings associate bus, target and LUN numbers with the LUNs on a target device.






## -see-also




<a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a>
 

 

