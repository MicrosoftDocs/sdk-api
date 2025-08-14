---
UID: NF:fileapi.SetFileIoOverlappedRange
title: SetFileIoOverlappedRange function (fileapi.h)
description: Associates a virtual address range with the specified file handle.
helpviewer_keywords: ["SetFileIoOverlappedRange","SetFileIoOverlappedRange function [Files]","fileapi/SetFileIoOverlappedRange","fs.setfileiooverlappedrange_func"]
old-location: fs\setfileiooverlappedrange_func.htm
tech.root: fs
ms.assetid: 4e7eff5e-2877-4524-8f76-55d41afe521d
ms.date: 12/05/2018
ms.keywords: SetFileIoOverlappedRange, SetFileIoOverlappedRange function [Files], fileapi/SetFileIoOverlappedRange, fs.setfileiooverlappedrange_func
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetFileIoOverlappedRange
 - fileapi/SetFileIoOverlappedRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetFileIoOverlappedRange
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
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetFileIoOverlappedRange</b> can be used to 
     improve performance in an application that issues a high number of asynchronous unbuffered I/O and uses a defined 
     range of overlapped structures. Because this range of structures is locked in memory, the kernel can avoid 
     acquiring certain locks when updating the overlapped structures with the results of the I/O request.

<b>SetFileIoOverlappedRange</b> requires the 
     caller to have the <a href="/windows/desktop/SecAuthZ/authorization-constants">SeLockMemoryPrivilege</a> 
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

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>