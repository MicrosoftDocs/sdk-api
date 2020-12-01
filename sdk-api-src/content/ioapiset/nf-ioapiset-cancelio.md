---
UID: NF:ioapiset.CancelIo
title: CancelIo function (ioapiset.h)
description: Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.
helpviewer_keywords: ["CancelIo","CancelIo function [Files]","_win32_cancelio","base.cancelio","fs.cancelio","ioapiset/CancelIo","winbase/CancelIo"]
old-location: fs\cancelio.htm
tech.root: fs
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
ms.date: 12/05/2018
ms.keywords: CancelIo, CancelIo function [Files], _win32_cancelio, base.cancelio, fs.cancelio, ioapiset/CancelIo, winbase/CancelIo
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
 - CancelIo
 - ioapiset/CancelIo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-io-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - CancelIo
---

# CancelIo function


## -description

Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file. The function does not cancel I/O operations that other threads issue for a file handle.

To cancel I/O operations from another thread, use the <a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a> function.

## -parameters

### -param hFile [in]

A handle to the file. 

The function cancels all pending I/O operations for this file handle.

## -returns

If the function succeeds, the return value is nonzero. The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested. The thread can use the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function to determine when the I/O operations themselves have been completed.

If the function fails, the return value is zero (0). To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the <b>CancelIo</b> function cancels them. <b>CancelIo</b> cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.

The I/O operations must be issued as overlapped I/O. If they are not, the I/O operations do not  return to allow the thread to call the 
<b>CancelIo</b> function. Calling the 
<b>CancelIo</b> function with a file handle that is not opened with <b>FILE_FLAG_OVERLAPPED</b> does nothing.

All I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>, and all completion notifications for the I/O operations occur normally.

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

<a href="/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a>



<a href="/windows/desktop/FileIO/cancelsynchronousio-func">CancelSynchronousIo</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-lockfileex">LockFileEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesw">ReadDirectoryChangesW</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>