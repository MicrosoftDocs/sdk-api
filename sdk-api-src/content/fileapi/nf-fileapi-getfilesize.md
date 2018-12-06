---
UID: NF:fileapi.GetFileSize
title: GetFileSize function
author: windows-sdk-content
description: Retrieves the size of the specified file, in bytes.
old-location: fs\getfilesize.htm
tech.root: fileio
ms.assetid: 3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFileSize, GetFileSize function [Files], _win32_getfilesize, base.getfilesize, fileapi/GetFileSize, fs.getfilesize, winbase/GetFileSize
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
 - GetFileSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFileSize function


## -description


Retrieves the size of the specified file, in bytes.

It is recommended that you use <a href="https://msdn.microsoft.com/782457bc-8f37-4eec-8ff3-b148fd0a7345">GetFileSizeEx</a>.


## -parameters




### -param hFile [in]

A handle to the file.


### -param lpFileSizeHigh [out, optional]

A pointer to the variable where the high-order doubleword of the file size is returned. This parameter can 
      be <b>NULL</b> if the application does not require the high-order doubleword.


## -returns



If the function succeeds, the return value is the low-order doubleword of the file size, and, if 
       <i>lpFileSizeHigh</i> is non-<b>NULL</b>, the function puts the 
       high-order doubleword of the file size into the variable pointed to by that parameter.

If the function fails and <i>lpFileSizeHigh</i> is <b>NULL</b>, the 
       return value is <b>INVALID_FILE_SIZE</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. When 
       <i>lpFileSizeHigh</i> is <b>NULL</b>, the results returned for large 
       files are ambiguous, and you will not be able to determine the actual size of the file. It is recommended that 
       you use <a href="https://msdn.microsoft.com/782457bc-8f37-4eec-8ff3-b148fd0a7345">GetFileSizeEx</a> instead.

If the function fails and <i>lpFileSizeHigh</i> is non-<b>NULL</b>, the 
       return value is <b>INVALID_FILE_SIZE</b> and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return a value other than 
       <b>NO_ERROR</b>.




## -remarks



You cannot use the <b>GetFileSize</b> function with a handle of 
    a nonseeking device such as a pipe or a communications device. To determine the file type for 
    <i>hFile</i>, use the <a href="https://msdn.microsoft.com/11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa">GetFileType</a> 
    function.

The <b>GetFileSize</b> function retrieves the uncompressed size 
    of a file. Use the <a href="https://msdn.microsoft.com/cca91080-2270-4996-8693-933c585ff168">GetCompressedFileSize</a> 
    function to obtain the compressed size of a file.

Note that if the return value is <b>INVALID_FILE_SIZE</b> (0xffffffff), an application must 
    call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to determine whether the function has 
    succeeded or failed. The reason the function may appear to fail when it has not is that 
    <i>lpFileSizeHigh</i> could be non-<b>NULL</b> or the file size could be 
    0xffffffff. In this case, <b>GetLastError</b> will return 
    <b>NO_ERROR</b> (0) upon success. Because of this behavior, it is recommended that you use 
    <a href="https://msdn.microsoft.com/782457bc-8f37-4eec-8ff3-b148fd0a7345">GetFileSizeEx</a> instead.

<b>Transacted Operations:  </b>If there is a transaction bound to the file handle, then the function returns information for the isolated 
      file view.

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
 


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/e47a0e79-3000-479b-afba-dcd36210ea3d">Creating a View Within a File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/cca91080-2270-4996-8693-933c585ff168">GetCompressedFileSize</a>



<a href="https://msdn.microsoft.com/782457bc-8f37-4eec-8ff3-b148fd0a7345">GetFileSizeEx</a>



<a href="https://msdn.microsoft.com/11760e2f-5e8b-4ec7-959b-fb23d5d9a0aa">GetFileType</a>
 

 

