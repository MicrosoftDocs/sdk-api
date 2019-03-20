---
UID: NF:memoryapi.FlushViewOfFile
title: FlushViewOfFile function (memoryapi.h)
author: windows-sdk-content
description: Writes to the disk a byte range within a mapped view of a file.
old-location: base\flushviewoffile.htm
tech.root: Memory
ms.assetid: 994fef62-77cf-4c99-be54-b4aff35a10f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FlushViewOfFile, FlushViewOfFile function, _win32_flushviewoffile, base.flushviewoffile, fs.flushviewoffile, winbase/FlushViewOfFile
ms.topic: function
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
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
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - FlushViewOfFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlushViewOfFile function


## -description


Writes to the disk a byte range within a mapped view of a file.


## -parameters




### -param lpBaseAddress [in]

A pointer to the base address of the byte range to be flushed to the disk representation of the mapped file.


### -param dwNumberOfBytesToFlush [in]

The number of bytes to be flushed. If <i>dwNumberOfBytesToFlush</i> is zero, the file is flushed from the base address to the end of the mapping.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Flushing a range of a mapped view initiates writing of dirty pages within that range to the disk. Dirty pages are those whose contents have changed since the file view was mapped. The <b>FlushViewOfFile</b> function does not flush the file metadata, and it does not wait to  return until  the changes are flushed from the underlying hardware disk cache and physically written to disk. To flush all the dirty pages plus the metadata for the file and ensure that they are physically written to disk, call <b>FlushViewOfFile</b> and then call the <a href="https://msdn.microsoft.com/0d9ea467-6d5d-44b2-8e87-f2ecdd510fe6">FlushFileBuffers</a> function.

When flushing a memory-mapped file over a network, 
<b>FlushViewOfFile</b> guarantees that the data has been written from the local computer, but not that the data resides on the remote computer. The server can cache the data on the remote side. Therefore, 
<b>FlushViewOfFile</b> can return before the data has been physically written to disk.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically.  If required, the caller should use <a href="https://msdn.microsoft.com/75d988e4-22a3-4084-a5f8-1fca73ccd542">SetFileTime</a> to set the timestamp.

In Windows Server 2012, this function is supported by the following technologies.

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
 

When CsvFs is paused this call might fail with an error indicating that there is a lock conflict.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/c2a3da09-d116-4c2c-9e6c-ec9e80c88b99">Reading and Writing From a File View</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4">Creating a File View</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">File Mapping Functions</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a>
 

 

