---
UID: NF:fileapi.ReadFileScatter
title: ReadFileScatter function
author: windows-sdk-content
description: Reads data from a file and stores it in an array of buffers.
old-location: fs\readfilescatter.htm
tech.root: fileio
ms.assetid: 4ed7c47b-d40b-4016-8550-0af17ee9e86d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ReadFileScatter, ReadFileScatter function [Files], _win32_readfilescatter, base.readfilescatter, fileapi/ReadFileScatter, fs.readfilescatter, winbase/ReadFileScatter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - ReadFileScatter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReadFileScatter function


## -description


Reads data from a file and stores it in an array of buffers.

The function starts reading data from the file at a position that is specified by an 
    <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. The 
    <b>ReadFileScatter</b> function operates asynchronously.


## -parameters




### -param hFile [in]

A handle to the file to be read.

The file handle must be created with the <b>GENERIC_READ</b> right, and the 
       <b>FILE_FLAG_OVERLAPPED</b> and <b>FILE_FLAG_NO_BUFFERING</b> flags. For 
       more information, see 
       <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param aSegmentArray [in]

A pointer to an array of <a href="https://msdn.microsoft.com/dde79dcb-95ec-4a9e-87a4-9ad99ac6266e">FILE_SEGMENT_ELEMENT</a> 
       buffers that receives the data. For a description of this union, see Remarks.

Each element can receive one page of data.

<div class="alert"><b>Note</b>  To determine the size of a system page, use 
       <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>.</div>
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

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> data 
       structure.

The <b>ReadFileScatter</b> function requires a valid 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. The 
       <i>lpOverlapped</i> parameter 
       cannot be <b>NULL</b>.

The <b>ReadFileScatter</b> function starts reading data 
       from the file at a position that is specified by the <b>Offset</b> and 
       <b>OffsetHigh</b> members of the 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.

The <b>ReadFileScatter</b> function may return before the 
       read operation is complete. In that scenario, the 
       <b>ReadFileScatter</b> function returns the value 0 
       (zero), and the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the 
       value <b>ERROR_IO_PENDING</b>. This asynchronous operation of 
       <b>ReadFileScatter</b> lets the calling process continue 
       while the read operation completes. You can call the 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>, 
       <a href="https://msdn.microsoft.com/1e2a3bf0-a73e-4406-99ac-32652f7f5b25">HasOverlappedIoCompleted</a>, or 
       <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> functions to 
       obtain information about the completion of the read operation. For more information, see 
       <a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

If <b>ReadFileScatter</b> attempts to read past the 
       end-of-file (EOF), the call to 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> for that operation returns 
       <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
       returns <b>ERROR_HANDLE_EOF</b>.

If the function returns before the read operation is complete, the function returns zero (0), and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_IO_PENDING</b>.




## -remarks



This function is not supported for 32-bit applications by WOW64 on Itanium-based systems.

The <a href="https://msdn.microsoft.com/dde79dcb-95ec-4a9e-87a4-9ad99ac6266e">FILE_SEGMENT_ELEMENT</a> union is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef union _FILE_SEGMENT_ELEMENT {
    PVOID64 Buffer;
    ULONGLONG Alignment;
}FILE_SEGMENT_ELEMENT, *PFILE_SEGMENT_ELEMENT;</pre>
</td>
</tr>
</table></span></div>
Assigning a pointer to the <b>Buffer</b> member will sign-extend the value if the code is 
     compiled as 32-bits; this can break large-address aware applications running on systems configured with 
     <a href="https://msdn.microsoft.com/991eb86f-9e6f-4084-8b6f-f979e42104b5">4-Gigabyte Tuning</a> or running on under WOW64 on 64-bit 
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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/dde79dcb-95ec-4a9e-87a4-9ad99ac6266e">FILE_SEGMENT_ELEMENT</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/1e2a3bf0-a73e-4406-99ac-32652f7f5b25">HasOverlappedIoCompleted</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/9590eabb-6e85-406e-8101-e67f87e6850b">WriteFileGather</a>
 

 

