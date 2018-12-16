---
UID: NF:fileapi.GetLogicalDriveStringsW
title: GetLogicalDriveStringsW function
author: windows-sdk-content
description: Fills a buffer with strings that specify valid drives in the system.
old-location: fs\getlogicaldrivestrings.htm
tech.root: fileio
ms.assetid: d3a83f8d-c37c-48b9-a24c-f81dfe5773e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLogicalDriveStrings, GetLogicalDriveStrings function [Files], GetLogicalDriveStringsA, GetLogicalDriveStringsW, _win32_getlogicaldrivestrings, base.getlogicaldrivestrings, fileapi/GetLogicalDriveStrings, fileapi/GetLogicalDriveStringsA, fileapi/GetLogicalDriveStringsW, fs.getlogicaldrivestrings, winbase/GetLogicalDriveStrings, winbase/GetLogicalDriveStringsA, winbase/GetLogicalDriveStringsW
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLogicalDriveStringsW (Unicode) and GetLogicalDriveStringsA (ANSI)
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
 - API-Ms-Win-Core-File-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetLogicalDriveStrings
 - GetLogicalDriveStringsA
 - GetLogicalDriveStringsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLogicalDriveStringsW function


## -description


Fills a buffer with strings that specify valid drives in the system.


## -parameters




### -param nBufferLength [in]

The maximum size of the buffer pointed to by <i>lpBuffer</i>, in 
      <b>TCHARs</b>. This size does not include the terminating null character. If this 
      parameter is zero, <i>lpBuffer</i> is not used.


### -param lpBuffer [out]

A pointer to a buffer that receives a series of null-terminated strings, one for each valid drive in the 
      system, plus with an additional null character. Each string is a device name.


## -returns



If the function succeeds, the return value is the length, in characters, of the strings copied to the buffer, 
       not including the terminating null character. Note that an ANSI-ASCII null character uses one byte, but a 
       Unicode (UTF-16) null character uses two bytes.

If the buffer is not large enough, the return value is greater than <i>nBufferLength</i>. 
       It is the size of the buffer required to hold the drive strings.

If the function fails, the return value is zero. To get extended error information, use the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



Each string in the buffer may be used wherever a root directory is required, such as for the 
    <a href="https://msdn.microsoft.com/b3989a3f-fc90-4ea0-8d3e-8e57068a08bc">GetDriveType</a> and 
    <a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a> functions.

This function returns a concatenation of the drives in the Global and Local MS-DOS Device namespaces. If a 
    drive exists in both namespaces, this function will return the entry in the Local MS-DOS Device namespace. For 
    more information, see 
    <a href="https://msdn.microsoft.com/7d802e9f-dc09-4e3d-b064-e9b57af396e2">Defining an MS DOS Device Name</a>.

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
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

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
 

SMB does not support volume management functions.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/359673bf-cc4c-4881-b946-ecdbef4a7ecb">Obtaining a File Name From a File Handle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4fe14c49-3fd6-48b7-92de-a0c867b2e042">GetDiskFreeSpace</a>



<a href="https://msdn.microsoft.com/b3989a3f-fc90-4ea0-8d3e-8e57068a08bc">GetDriveType</a>



<a href="https://msdn.microsoft.com/21a66050-3bab-4c70-9003-3b52e8c72b00">GetLogicalDrives</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

