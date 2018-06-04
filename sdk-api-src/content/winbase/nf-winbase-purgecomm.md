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

# PurgeComm function


## -description


Discards all characters from the output or input buffer of a specified communications resource. It can also terminate pending read or write operations on the resource.


## -parameters




### -param hFile [in]

A handle to the communications resource. The 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function returns this handle.


### -param dwFlags [in]

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PURGE_RXABORT"></a><a id="purge_rxabort"></a><dl>
<dt><b>PURGE_RXABORT</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Terminates all outstanding overlapped read operations and returns immediately, even if the read operations have not been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="PURGE_RXCLEAR"></a><a id="purge_rxclear"></a><dl>
<dt><b>PURGE_RXCLEAR</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Clears the input buffer (if the device driver has one).

</td>
</tr>
<tr>
<td width="40%"><a id="PURGE_TXABORT"></a><a id="purge_txabort"></a><dl>
<dt><b>PURGE_TXABORT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Terminates all outstanding overlapped write operations and returns immediately, even if the write operations have not been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="PURGE_TXCLEAR"></a><a id="purge_txclear"></a><dl>
<dt><b>PURGE_TXCLEAR</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Clears the output buffer (if the device driver has one).

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a thread uses 
<b>PurgeComm</b> to flush an output buffer, the deleted characters are not transmitted. To empty the output buffer while ensuring that the contents are transmitted, call the 
<a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a> function (a synchronous operation). Note, however, that <b>FlushFileBuffers</b> is subject to flow control but not to write time-outs, and it will not return until all pending write operations have been transmitted.




## -see-also




<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>
 

 

