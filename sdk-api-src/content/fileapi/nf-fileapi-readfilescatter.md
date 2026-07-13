---
UID: NF:fileapi.ReadFileScatter
title: ReadFileScatter function (fileapi.h)
description: Reads data from a file and stores it in an array of buffers.
helpviewer_keywords: ["ReadFileScatter","ReadFileScatter function [Files]","_win32_readfilescatter","base.readfilescatter","fileapi/ReadFileScatter","fs.readfilescatter","winbase/ReadFileScatter"]
old-location: fs\readfilescatter.htm
tech.root: fs
ms.assetid: 4ed7c47b-d40b-4016-8550-0af17ee9e86d
ms.date: 08/16/2022
ms.keywords: ReadFileScatter, ReadFileScatter function [Files], _win32_readfilescatter, base.readfilescatter, fileapi/ReadFileScatter, fs.readfilescatter, winbase/ReadFileScatter
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ReadFileScatter
 - fileapi/ReadFileScatter
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - ReadFileScatter
---

# ReadFileScatter function


## -description

Reads data from a file and stores it in an array of buffers.

The function starts reading data from the file at a position that is specified by an 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The 
    **ReadFileScatter** function operates asynchronously.

## -parameters

### -param hFile [in]

A handle to the file to be read.

The file handle must be created with the **GENERIC_READ** right, and the **FILE_FLAG_OVERLAPPED** and **FILE_FLAG_NO_BUFFERING** flags. For more information, see <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param aSegmentArray [in]

A pointer to an array of [FILE_SEGMENT_ELEMENT structure](../winnt/ns-winnt-file_segment_element.md)  buffers that receives the data. For a description of this union, see [Remarks](#remarks).

Each element represents one page of data.

> [!NOTE]
> To determine the size of a system page, use <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>.

The array must contain enough elements to represent *nNumberOfBytesToRead* bytes of data. For example, if there are 40 KB to be read and the page size is 4 KB, the array must have 10 elements.

Each buffer must be at least the size of a system memory page and must be aligned on a system memory page size boundary. The system reads one system memory page of data into each buffer.

The function stores the data in the buffers in sequential order. For example, it stores data into the first buffer, then into the second buffer, and so on until each buffer is filled and all the data is stored, or *nNumberOfBytesToRead* bytes have been read.

### -param nNumberOfBytesToRead [in]

The total number of bytes to be read from the file. Each element of *aSegmentArray* contains a one-page chunk of this total. Because the file must be opened with **FILE_FLAG_NO_BUFFERING**, the number of bytes must be a multiple of the sector size of the file system where the file is located.

### -param lpReserved

This parameter is reserved for future use and must be **NULL**.

### -param lpOverlapped [in, out]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> data structure.

The **ReadFileScatter** function requires a valid 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The *lpOverlapped* parameter cannot be **NULL**.

The **ReadFileScatter** function starts reading data from the file at a position that is specified by the **Offset** and **OffsetHigh** members of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

The **ReadFileScatter** function may return before the read operation is complete. In that scenario, the **ReadFileScatter** function returns the value 0 (zero), and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the value **ERROR_IO_PENDING**. This asynchronous operation of **ReadFileScatter** lets the calling process continue while the read operation completes. You can call the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>, <a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>, or <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> functions to obtain information about the completion of the read operation. For more information, see <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If **ReadFileScatter** attempts to read past the end-of-file (EOF), the call to <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> for that operation returns **FALSE** and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns **ERROR_HANDLE_EOF**.

If the function returns before the read operation is complete, the function returns zero (0), and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns **ERROR_IO_PENDING**.

## -remarks

This function is not supported for 32-bit applications by WOW64 on Itanium-based systems.

The [FILE_SEGMENT_ELEMENT structure](../winnt/ns-winnt-file_segment_element.md) is defined as follows:


```cpp
typedef union _FILE_SEGMENT_ELEMENT {
    PVOID64 Buffer;
    ULONGLONG Alignment;
}FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT;
```

Assigning a pointer to the **Buffer** member will sign-extend the value if the code is compiled as 32-bits; this can break large-address aware applications running on systems configured with <a href="/windows/desktop/Memory/4-gigabyte-tuning">4-Gigabyte Tuning</a> or running on under WOW64 on 64-bit Windows. Therefore, use the **PtrToPtr64** macro when assigning pointers to **Buffer**.

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
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the file handle, then the function returns data from the transacted view of 
      the file. A transacted read handle is guaranteed to show the same view of a file for the duration of the 
      handle.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winnt/ns-winnt-file_segment_element.md">FILE_SEGMENT_ELEMENT</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefilegather">WriteFileGather</a>