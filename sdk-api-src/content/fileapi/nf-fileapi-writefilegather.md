---
UID: NF:fileapi.WriteFileGather
title: WriteFileGather function (fileapi.h)
description: Retrieves data from an array of buffers and writes the data to a file.
helpviewer_keywords: ["WriteFileGather","WriteFileGather function [Files]","_win32_writefilegather","base.writefilegather","fileapi/WriteFileGather","fs.writefilegather","winbase/WriteFileGather"]
old-location: fs\writefilegather.htm
tech.root: fs
ms.assetid: 9590eabb-6e85-406e-8101-e67f87e6850b
ms.date: 12/05/2018
ms.keywords: WriteFileGather, WriteFileGather function [Files], _win32_writefilegather, base.writefilegather, fileapi/WriteFileGather, fs.writefilegather, winbase/WriteFileGather
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
 - WriteFileGather
 - fileapi/WriteFileGather
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
 - WriteFileGather
---

# WriteFileGather function

## -description

Retrieves data from an array of buffers and writes the data to a file.

The function starts writing data to the file at a position that is specified by an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The **WriteFileGather** function operates asynchronously.

## -parameters

### -param hFile [in]

A handle to the file. The file handle must be created with the **GENERIC_WRITE** access right, and the **FILE_FLAG_OVERLAPPED** and **FILE_FLAG_NO_BUFFERING** flags. For more information, see <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param aSegmentArray [in]

A pointer to an array of [FILE_SEGMENT_ELEMENT structure](../winnt/ns-winnt-file_segment_element.md) buffers that contain the data. For a description of this union, see Remarks.

Each element represents one page of data.

> [!NOTE]
> To determine the size of a system page, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function.

The array must contain enough elements to represent *nNumberOfBytesToWrite* bytes of data. For example, if there are 40 KB to be written and the page size is 4 KB, the array must have 10 elements.

Each buffer must be at least the size of a system memory page and must be aligned on a system memory page size boundary. The system writes one system memory page of data from each buffer.

The function gathers the data from the buffers in sequential order. For example, it writes data to the file from the first buffer, then the second buffer, and so on until *nNumberOfBytesToWrite* bytes have been written.

Due to the asynchronous operation of this function, precautions must be taken to ensure that this parameter always references valid memory for the lifetime of the asynchronous writes. For instance, a common programming error is to use local stack storage and then allow execution to run out of scope.

### -param nNumberOfBytesToWrite [in]

The total number of bytes to be written. Each element of *aSegmentArray* contains a one-page chunk of this total. Because the file must be opened with **FILE_FLAG_NO_BUFFERING**, the number of bytes must be a multiple of the sector size of the file system where the file is located.

If *nNumberOfBytesToWrite* is zero (0), the function performs a null write operation. The behavior of a null write operation depends on the underlying file system. If *nNumberOfBytesToWrite* is not zero (0) and the offset and length of the write place data beyond the current end of the file, the **WriteFileGather** function extends the file.

### -param lpReserved

This parameter is reserved for future use and must be **NULL**.

### -param lpOverlapped [in, out]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> data structure.

The **WriteFileGather** function requires a valid 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The *lpOverlapped* parameter cannot be **NULL**.

The **WriteFileGather** function starts writing data to the file at a position that is specified by the **Offset** and **OffsetHigh** members of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

The **WriteFileGather** function may return before the write operation is complete. In that scenario, the **WriteFileGather** function returns the value zero (0), and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns the value **ERROR_IO_PENDING**. This asynchronous operation of the **WriteFileGather** function lets the calling process continue while the write operation completes. 

You can call the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>, <a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>, or <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function to obtain information about the completion of the write operation. For more information, see <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If the function returns before the write operation is complete, the function returns zero (0), and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns **ERROR_IO_PENDING**.

## -remarks

This function is not supported for 32-bit applications by WOW64 on the Itanium-based systems.

The [FILE_SEGMENT_ELEMENT structure](../winnt/ns-winnt-file_segment_element.md) is defined as follows:

```cpp
typedef union _FILE_SEGMENT_ELEMENT {
    PVOID64   Buffer;
    ULONGLONG Alignment;
}FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT;
```

Assigning a pointer to the **Buffer** member will sign-extend the value if the code is compiled as 32-bits; this can break large-address aware applications running on systems configured with <a href="/windows/desktop/Memory/4-gigabyte-tuning">4-Gigabyte Tuning</a> or running under WOW64 on 64-bit Windows. Therefore, use the **PtrToPtr64** macro when assigning pointers to **Buffer**.

If part of the file specified by *hFile* is locked by another process, and the write operation overlaps the locked portion, the **WriteFileGather** function fails.

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
If there is a transaction bound to the file handle, then the operation is transacted.

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfilescatter">ReadFileScatter</a>



<a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>