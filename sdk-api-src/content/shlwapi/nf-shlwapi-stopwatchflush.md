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

# StopWatchFlush function


## -description


<p class="CCE_Message">[<b>StopWatchFlush</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Writes out performance statistics if performance logging is enabled.


## -parameters






## -returns



Type: <b>DWORD</b>

ERROR_SUCCESS on success, or an error code on failure. Possible error codes include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
No performance logs were collected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
Performance logging is not enabled.

</td>
</tr>
</table>
 




## -remarks



The performance log is written to the shperf.log file in the Windows directory.  If message performance logs are enabled, the message performance log is written to the msgtrace.log file in the Windows directory. If you call <b>StopWatchFlush</b>, you must have permission to create and modify files in the Windows directory.

Calling <b>StopWatchFlush</b> clears the performance logs after writing them to the shperf.log file.

See the <a href="https://msdn.microsoft.com/3db69040-0720-41a3-ba88-db885a2685aa">StopWatchMode</a> function for a description of the information that is recorded in the performance log.



