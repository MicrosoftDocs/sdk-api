---
UID: NF:fileapi.SetFileIoOverlappedRange
title: SetFileIoOverlappedRange function
author: windows-sdk-content
description: Associates a virtual address range with the specified file handle.
old-location: fs\setfileiooverlappedrange_func.htm
tech.root: fileio
ms.assetid: 4e7eff5e-2877-4524-8f76-55d41afe521d
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SetFileIoOverlappedRange, SetFileIoOverlappedRange function [Files], fileapi/SetFileIoOverlappedRange, fs.setfileiooverlappedrange_func
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - API-MS-Win-Core-File-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetFileIoOverlappedRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFileIoOverlappedRange function


## -description


 Associates a virtual address range with the specified file handle. This indicates that the 
    kernel should optimize any further asynchronous I/O requests with overlapped structures inside this range. The 
    overlapped range is locked in memory, and then unlocked when the file is closed. After a range is associated with 
    a file handle, it cannot be disassociated.


## -parameters




### -param FileHandle [in]

A handle to the file.

This file handle must be opened with <b>FILE_READ_ATTRIBUTES</b> access rights.


### -param OverlappedRangeStart [in]

The starting address for the range.


### -param Length [in]

The length of the range, in bytes.


## -returns



Returns nonzero if successful or zero otherwise.

To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>SetFileIoOverlappedRange</b> can be used to 
     improve performance in an application that issues a high number of asynchronous unbuffered I/O and uses a defined 
     range of overlapped structures. Because this range of structures is locked in memory, the kernel can avoid 
     acquiring certain locks when updating the overlapped structures with the results of the I/O request.

<b>SetFileIoOverlappedRange</b> requires the 
     caller to have the <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeLockMemoryPrivilege</a> 
     access privilege.

This function has no effect on buffered and synchronous I/O.

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
 




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>
 

 

