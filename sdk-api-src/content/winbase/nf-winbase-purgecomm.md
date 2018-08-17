---
UID: NF:winbase.PurgeComm
title: PurgeComm function
author: windows-sdk-content
description: Discards all characters from the output or input buffer of a specified communications resource. It can also terminate pending read or write operations on the resource.
old-location: base\purgecomm.htm
old-project: devio
ms.assetid: bfbd6530-447e-46e2-89e6-683b3c8c32ea
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PURGE_RXABORT, PURGE_RXCLEAR, PURGE_TXABORT, PURGE_TXCLEAR, PurgeComm, PurgeComm function, _win32_purgecomm, base.purgecomm, winbase/PurgeComm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - PurgeComm
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PurgeComm function


## -description


Discards all characters from the output or input buffer of a specified communications resource. It can also terminate pending read or write operations on the resource.


## -parameters




### -param hFile [in]

A handle to the communications resource. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


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



<a href="base.createfile">CreateFile</a>
 

 

