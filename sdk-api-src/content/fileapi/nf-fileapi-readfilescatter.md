---
UID: NF:fileapi.ReadFileScatter
title: ReadFileScatter function (fileapi.h)
description: Reads data from a file and stores it in an array of buffers.
helpviewer_keywords: ["ReadFileScatter","ReadFileScatter function [Files]","_win32_readfilescatter","base.readfilescatter","fileapi/ReadFileScatter","fs.readfilescatter","winbase/ReadFileScatter"]
old-location: fs\readfilescatter.htm
tech.root: fs
ms.assetid: 4ed7c47b-d40b-4016-8550-0af17ee9e86d
ms.date: 12/05/2018
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
    <b>ReadFileScatter</b> function operates asynchronously.

## -parameters

### -param hFile [in]

A handle to the file to be read.

The file handle must be created with the <b>GENERIC_READ</b> right, and the 
       <b>FILE_FLAG_OVERLAPPED</b> and <b>FILE_FLAG_NO_BUFFERING</b> flags. For 
       more information, see 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param aSegmentArray [in]

A pointer to an array of <a href="/windows/desktop/api/winnt/ns-winnt-_file_segment_element">FILE_SEGMENT_ELEMENT</a> 
       buffers that receives the data. For a description of this union, see Remarks.

Each element can receive one page of data.

<div class="alert"><b>Note</b>  To determine the size of a system page, use 
       <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>.</div>
<div> </div>
The array must contain enough elements to store <i>nNumberOfBytesToRead</i> bytes of data, 
       plus one element for the terminating <b>NULL</b>. For example, if there are 40 KB to be 
       read and the page size is 4 KB, the array must have 11 elements that includes 10 for the data and one for 
       the <b>NULL</b>.

Each buffer must be at least the size of a system memory page and must be aligned on a system memory page 
       size boundary. The system reads one system memory page of data into each buffer.

The function stores the data in the buffers in sequential order. For example, it stores data into the first 
       buffer, then into the second buffer, and so on until each buffer is filled and all the data is stored, or there 
       are no more buffers.

### -param nNumberOfBytesToRead [in]

The total number of bytes to be read from the file. Each element of <i>aSegmentArray</i> 
      contains a one-page chunk of this total. Because the file must be opened with 
      <b>FILE_FLAG_NO_BUFFERING</b>, the number of bytes must be a multiple of the sector size of 
      the file system where the file is located.

### -param lpReserved

This parameter is reserved for future use and must be <b>NULL</b>.

### -param lpOverlapped [in, out]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> data 
       structure.

The <b>ReadFileScatter</b> function requires a valid 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The 
       <i>lpOverlapped</i> parameter 
       cannot be <b>NULL</b>.

The <b>ReadFileScatter</b> function starts reading data 
       from the file at a position that is specified by the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

The <b>ReadFileScatter</b> function may return before the 
       read operation is complete. In that scenario, the 
       <b>ReadFileScatter</b> function returns the value 0 
       (zero), and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the 
       value <b>ERROR_IO_PENDING</b>. This asynchronous operation of 
       <b>ReadFileScatter</b> lets the calling process continue 
       while the read operation completes. You can call the 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>, 
       <a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>, or 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> functions to 
       obtain information about the completion of the read operation. For more information, see 
       <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If <b>ReadFileScatter</b> attempts to read past the 
       end-of-file (EOF), the call to 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> for that operation returns 
       <b>FALSE</b> and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       returns <b>ERROR_HANDLE_EOF</b>.

If the function returns before the read operation is complete, the function returns zero (0), and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_IO_PENDING</b>.

## -remarks

This function is not supported for 32-bit applications by WOW64 on Itanium-based systems.

The <a href="/windows/desktop/api/winnt/ns-winnt-_file_segment_element">FILE_SEGMENT_ELEMENT</a> union is defined as follows:


```cpp
typedef union _FILE_SEGMENT_ELEMENT {
    PVOID64 Buffer;
    ULONGLONG Alignment;
}FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT;
```


Assigning a pointer to the <b>Buffer</b> member will sign-extend the value if the code is 
     compiled as 32-bits; this can break large-address aware applications running on systems configured with 
     <a href="/windows/desktop/Memory/4-gigabyte-tuning">4-Gigabyte Tuning</a> or running on under WOW64 on 64-bit 
     Windows. Therefore, use the <b>PtrToPtr64</b> macro when assigning pointers to 
     <b>Buffer</b>.

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



<a href="/windows/desktop/api/winnt/ns-winnt-_file_segment_element">FILE_SEGMENT_ELEMENT</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefilegather">WriteFileGather</a>