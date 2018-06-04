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

# _SMGRSTATUS structure


## -description


Contains status information used by the 
<a href="https://msdn.microsoft.com/46f0094d-9079-41b5-9efc-ef07082653d3">SRSetRestorePoint</a> function.


## -struct-fields




### -field nStatus

The status code. For a list of values, see the Remarks section.


### -field llSequenceNumber

The sequence number of the restore point.


## -remarks



The following table lists the status codes returned in the <b>nStatus</b> member. Note that all the status codes indicate failure except ERROR_SUCCESS.

<table>
<tr>
<th>Status Code</th>
<th>Meaning</th>
</tr>
<tr>
<td>ERROR_SUCCESS</td>
<td>The call succeeded.</td>
</tr>
<tr>
<td>ERROR_BAD_ENVIRONMENT</td>
<td>The function was called in safe mode.</td>
</tr>
<tr>
<td>ERROR_DISK_FULL</td>
<td>System Restore is in standby mode because disk space is low.</td>
</tr>
<tr>
<td>ERROR_INTERNAL_ERROR</td>
<td>An internal error occurred.</td>
</tr>
<tr>
<td>ERROR_INVALID_DATA</td>
<td>The sequence number is invalid.</td>
</tr>
<tr>
<td>ERROR_SERVICE_DISABLED</td>
<td>System Restore is disabled.</td>
</tr>
<tr>
<td>ERROR_TIMEOUT</td>
<td>The call timed out due to a wait on a mutex for setting restore points.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/46f0094d-9079-41b5-9efc-ef07082653d3">SRSetRestorePoint</a>
 

 

