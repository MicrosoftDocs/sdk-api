---
UID: NS:srrestoreptapi._SMGRSTATUS
title: "_SMGRSTATUS"
author: windows-sdk-content
description: Contains status information used by the SRSetRestorePoint function.
old-location: sr\statemgrstatus_str.htm
tech.root: sr
ms.assetid: 3531474b-1499-4c83-ab32-8c464c0eece0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSTATEMGRSTATUS, PSTATEMGRSTATUS, PSTATEMGRSTATUS structure pointer [System Restore], STATEMGRSTATUS, STATEMGRSTATUS structure [System Restore], _SMGRSTATUS, _sr_statemgrstatus_str, sr.statemgrstatus_str, srrestoreptapi/PSTATEMGRSTATUS, srrestoreptapi/STATEMGRSTATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: srrestoreptapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SRRestorePtAPI.h
api_name:
 - STATEMGRSTATUS
product: Windows
targetos: Windows
req.typenames: STATEMGRSTATUS, *PSTATEMGRSTATUS
req.redist: 
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
 

 

