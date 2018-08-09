---
UID: NF:fileapi.WriteFileGather
title: WriteFileGather function
author: windows-sdk-content
description: Retrieves data from an array of buffers and writes the data to a file.
old-location: fs\writefilegather.htm
old-project: fileio
ms.assetid: 9590eabb-6e85-406e-8101-e67f87e6850b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WriteFileGather, WriteFileGather function [Files], _win32_writefilegather, base.writefilegather, fileapi/WriteFileGather, fs.writefilegather, winbase/WriteFileGather
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: STREAM_INFO_LEVELS
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
 - WriteFileGather
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# WriteFileGather function


## -description


Retrieves data 
    from an array of buffers and writes the data to a file.

The function starts writing data to the file at a position that is specified by an 
    <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. The 
    <b>WriteFileGather</b> function operates asynchronously.


## -parameters




### -param hFile [in]

A handle to the file. The file handle must be created with the <b>GENERIC_WRITE</b> 
      access right, and the <b>FILE_FLAG_OVERLAPPED</b> and 
      <b>FILE_FLAG_NO_BUFFERING</b> flags. For more information, see 
      <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param aSegmentArray [in]

A pointer to an array of <a href="https://msdn.microsoft.com/dde79dcb-95ec-4a9e-87a4-9ad99ac6266e">FILE_SEGMENT_ELEMENT</a> 
       buffers that contain the data. For a description of this union, see Remarks.

Each element contains the address of one page of data. 
       <div class="alert"><b>Note</b>  To determine the size of a system page, use the 
        <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function.</div>
<div> </div>The array must contain enough elements to store <i>nNumberOfBytesToWrite</i> bytes of data, 
       and one element for the terminating <b>NULL</b>. For example, if there are 40 KB to be read 
       and the page size is 4 KB, the array must have 11 elements that includes 10 elements for the data and one 
       element for the <b>NULL</b>.

Each buffer must be at least the size of a system memory page and must be aligned on a system memory page 
       size boundary. The system writes one system memory page of data from each buffer.

The function gathers the data from the buffers in a sequential order. For example, it writes data to the file 
       from the first buffer, then the second buffer, and so on until there is no more data.

Due to the asynchronous operation of this function, precautions must be taken to ensure that this parameter 
       always references valid memory for the lifetime of the asynchronous writes. For instance, a common programming 
       error is to use local stack storage and then allow execution to run out of scope.


### -param nNumberOfBytesToWrite [in]

The total number of bytes to be written. Each element of <i>aSegmentArray</i> contains a 
       one-page chunk of this total. Because the file must be opened with 
       <b>FILE_FLAG_NO_BUFFERING</b>, the number of bytes must be a multiple of the sector size of 
       the file system where the file is located.

If <i>nNumberOfBytesToWrite</i> is zero (0), the function performs a null write operation. 
       The behavior of a null write operation depends on the underlying file system. If 
       <i>nNumberOfBytesToWrite</i> is not zero (0) and the offset and length of the write place 
       data beyond the current end of the file, 
       the <b>WriteFileGather</b> function extends the file.


### -param lpReserved

This parameter is reserved for future use and must be <b>NULL</b>.


### -param lpOverlapped [in, out]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data 
       structure.

The <b>WriteFileGather</b> function requires a valid 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. The 
       <i>lpOverlapped</i> parameter cannot be <b>NULL</b>.

The <b>WriteFileGather</b> function starts writing data to 
       the file at a position that is specified by the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.

The <b>WriteFileGather</b> function may return before the 
       write operation is complete. In that scenario, the 
       <b>WriteFileGather</b> function returns the value zero (0), 
       and the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the 
       value <b>ERROR_IO_PENDING</b>. This asynchronous operation of the 
       <b>WriteFileGather</b> function lets the calling process 
       continue while the write operation completes. You can call the 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>, 
       <a href="https://msdn.microsoft.com/1e2a3bf0-a73e-4406-99ac-32652f7f5b25">HasOverlappedIoCompleted</a>, or 
       <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function to 
       obtain information about the completion of the write operation. For more information, see 
       <a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

If the function returns before the write operation is complete, the function returns zero (0), and 
       the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns 
       <b>ERROR_IO_PENDING</b>.




## -remarks



This function is not supported for 32-bit applications by WOW64 on the Itanium-based systems.

The <a href="https://msdn.microsoft.com/dde79dcb-95ec-4a9e-87a4-9ad99ac6266e">FILE_SEGMENT_ELEMENT</a> union is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef union _FILE_SEGMENT_ELEMENT {
    PVOID64   Buffer;
    ULONGLONG Alignment;
}FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT;</pre>
</td>
</tr>
</table></span></div>
Assigning a pointer to the <b>Buffer</b> member will sign-extend the value if the code is 
     compiled as 32-bits; this can break large-address aware applications running on systems configured with 
     <a href="https://msdn.microsoft.com/991eb86f-9e6f-4084-8b6f-f979e42104b5">4-Gigabyte Tuning</a> or running under WOW64 on 64-bit 
     Windows. Therefore, use the <b>PtrToPtr64</b> macro when assigning pointers to 
     <b>Buffer</b>.

If part of the file specified by <i>hFile</i> is locked by another process, and the write 
    operation overlaps the locked portion, the 
    <b>WriteFileGather</b> function fails.

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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/dde79dcb-95ec-4a9e-87a4-9ad99ac6266e">FILE_SEGMENT_ELEMENT</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/1e2a3bf0-a73e-4406-99ac-32652f7f5b25">HasOverlappedIoCompleted</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/4ed7c47b-d40b-4016-8550-0af17ee9e86d">ReadFileScatter</a>



<a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>
 

 

