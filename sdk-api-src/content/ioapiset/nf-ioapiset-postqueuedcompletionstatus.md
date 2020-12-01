---
UID: NF:ioapiset.PostQueuedCompletionStatus
title: PostQueuedCompletionStatus function (ioapiset.h)
description: Posts an I/O completion packet to an I/O completion port.
helpviewer_keywords: ["PostQueuedCompletionStatus","PostQueuedCompletionStatus function [Files]","_win32_postqueuedcompletionstatus","base.postqueuedcompletionstatus","fs.postqueuedcompletionstatus","ioapiset/PostQueuedCompletionStatus","winbase/PostQueuedCompletionStatus"]
old-location: fs\postqueuedcompletionstatus.htm
tech.root: fs
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
ms.date: 12/05/2018
ms.keywords: PostQueuedCompletionStatus, PostQueuedCompletionStatus function [Files], _win32_postqueuedcompletionstatus, base.postqueuedcompletionstatus, fs.postqueuedcompletionstatus, ioapiset/PostQueuedCompletionStatus, winbase/PostQueuedCompletionStatus
req.header: ioapiset.h
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
 - PostQueuedCompletionStatus
 - ioapiset/PostQueuedCompletionStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-io-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-io-l1-1-1.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - PostQueuedCompletionStatus
---

# PostQueuedCompletionStatus function


## -description

Posts an I/O completion packet to an I/O completion port.

## -parameters

### -param CompletionPort [in]

A handle to an I/O completion port to which the I/O completion packet is to be posted.

### -param dwNumberOfBytesTransferred [in]

The value to be returned through the <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

### -param dwCompletionKey [in]

The value to be returned through the <i>lpCompletionKey</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

### -param lpOverlapped [in, optional]

The value to be returned through the <i>lpOverlapped</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> .

## -remarks

The I/O completion packet will satisfy an outstanding call to the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function. This function returns with the three values passed as the second, third, and fourth parameters of the call to 
<b>PostQueuedCompletionStatus</b>. The system does not use or validate these values. In particular, the <i>lpOverlapped</i> parameter need not point to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 

CsvFs will do redirected IO for compressed files.

## -see-also

<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>