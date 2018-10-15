---
UID: NF:fileapi.GetFileInformationByHandle
title: GetFileInformationByHandle function
author: windows-sdk-content
description: Retrieves file information for the specified file.
old-location: fs\getfileinformationbyhandle.htm
tech.root: FileIO
ms.assetid: d026ee3a-c165-42a2-a4e1-efccdafbefc5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetFileInformationByHandle, GetFileInformationByHandle function [Files], _win32_getfileinformationbyhandle, base.getfileinformationbyhandle, fileapi/GetFileInformationByHandle, fs.getfileinformationbyhandle, winbase/GetFileInformationByHandle
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
 - GetFileInformationByHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFileInformationByHandle function


## -description


Retrieves file information for the specified file.

For a more advanced version of this function, see 
    <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>.

To set file information using a file handle, see 
    <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>.


## -parameters




### -param hFile [in]

A handle to the file that contains the information to be retrieved.

This handle should not be a pipe handle.


### -param lpFileInformation [out]

A pointer to a 
      <a href="https://msdn.microsoft.com/a6fc5cf0-d3b0-4a76-af8b-6a13ab32157d">BY_HANDLE_FILE_INFORMATION</a> structure that 
      receives the file information.


## -returns



If the function succeeds, the return value is nonzero and file information data is contained in the buffer 
       pointed to by the <i>lpFileInformation</i> parameter.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Depending on the underlying network features of the operating system and the type of server connected to, the 
    <b>GetFileInformationByHandle</b> function may fail, 
    return partial information, or full information for the given file.

You can compare the <b>VolumeSerialNumber</b> and <b>FileIndex</b> 
    members returned in the 
    <a href="https://msdn.microsoft.com/a6fc5cf0-d3b0-4a76-af8b-6a13ab32157d">BY_HANDLE_FILE_INFORMATION</a> structure to 
    determine if two paths map to the same target; for example, you can compare two file paths and determine if they 
    map to the same directory.

IIn Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
If there is a transaction bound to the thread at the time of the call, then the function returns the 
      compressed file size of the isolated file view. For more information, see 
      <a href="https://msdn.microsoft.com/52341315-0412-4a87-aca0-9adea7aae62f">About Transactional NTFS</a>.




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

