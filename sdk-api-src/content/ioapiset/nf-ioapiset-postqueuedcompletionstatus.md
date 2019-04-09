---
UID: NF:ioapiset.PostQueuedCompletionStatus
title: PostQueuedCompletionStatus function (ioapiset.h)
author: windows-sdk-content
description: Posts an I/O completion packet to an I/O completion port.
old-location: fs\postqueuedcompletionstatus.htm
tech.root: FileIO
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PostQueuedCompletionStatus, PostQueuedCompletionStatus function [Files], _win32_postqueuedcompletionstatus, base.postqueuedcompletionstatus, fs.postqueuedcompletionstatus, ioapiset/PostQueuedCompletionStatus, winbase/PostQueuedCompletionStatus
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PostQueuedCompletionStatus function


## -description


Posts an I/O completion packet to an I/O completion port.


## -parameters




### -param CompletionPort [in]

A handle to an I/O completion port to which the I/O completion packet is to be posted.


### -param dwNumberOfBytesTransferred [in]

The value to be returned through the <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


### -param dwCompletionKey [in]

The value to be returned through the <i>lpCompletionKey</i> parameter of the 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


### -param lpOverlapped [in, optional]

The value to be returned through the <i>lpOverlapped</i> parameter of the 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> .




## -remarks



The I/O completion packet will satisfy an outstanding call to the 
<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function. This function returns with the three values passed as the second, third, and fourth parameters of the call to 
<b>PostQueuedCompletionStatus</b>. The system does not use or validate these values. In particular, the <i>lpOverlapped</i> parameter need not point to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.

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




<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

