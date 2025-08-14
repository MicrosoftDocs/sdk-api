---
UID: NF:winbase.PurgeComm
title: PurgeComm function (winbase.h)
description: Discards all characters from the output or input buffer of a specified communications resource. It can also terminate pending read or write operations on the resource.
helpviewer_keywords: ["PURGE_RXABORT","PURGE_RXCLEAR","PURGE_TXABORT","PURGE_TXCLEAR","PurgeComm","PurgeComm function","_win32_purgecomm","base.purgecomm","winbase/PurgeComm"]
old-location: base\purgecomm.htm
tech.root: base
ms.assetid: bfbd6530-447e-46e2-89e6-683b3c8c32ea
ms.date: 12/05/2018
ms.keywords: PURGE_RXABORT, PURGE_RXCLEAR, PURGE_TXABORT, PURGE_TXCLEAR, PurgeComm, PurgeComm function, _win32_purgecomm, base.purgecomm, winbase/PurgeComm
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PurgeComm
 - winbase/PurgeComm
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - PurgeComm
---

# PurgeComm function


## -description

Discards all characters from the output or input buffer of a specified communications resource. It can also terminate pending read or write operations on the resource.

## -parameters

### -param hFile [in]

A handle to the communications resource. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a thread uses 
<b>PurgeComm</b> to flush an output buffer, the deleted characters are not transmitted. To empty the output buffer while ensuring that the contents are transmitted, call the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function (a synchronous operation). Note, however, that <b>FlushFileBuffers</b> is subject to flow control but not to write time-outs, and it will not return until all pending write operations have been transmitted.

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>