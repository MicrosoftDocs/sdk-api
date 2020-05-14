---
UID: NF:winbase.GetLogicalDriveStringsA
title: GetLogicalDriveStringsA function (winbase.h)
description: Fills a buffer with strings that specify valid drives in the system.helpviewer_keywords: ["GetLogicalDriveStrings","GetLogicalDriveStrings function [Files]","GetLogicalDriveStringsA","GetLogicalDriveStringsW","_win32_getlogicaldrivestrings","base.getlogicaldrivestrings","fileapi/GetLogicalDriveStrings","fileapi/GetLogicalDriveStringsA","fileapi/GetLogicalDriveStringsW","fs.getlogicaldrivestrings","winbase/GetLogicalDriveStrings","winbase/GetLogicalDriveStringsA","winbase/GetLogicalDriveStringsW"]
old-location: fs\getlogicaldrivestrings.htm
tech.root: FileIO
ms.assetid: d3a83f8d-c37c-48b9-a24c-f81dfe5773e9
ms.date: 12/05/2018
ms.keywords: GetLogicalDriveStrings, GetLogicalDriveStrings function [Files], GetLogicalDriveStringsA, GetLogicalDriveStringsW, _win32_getlogicaldrivestrings, base.getlogicaldrivestrings, fileapi/GetLogicalDriveStrings, fileapi/GetLogicalDriveStringsA, fileapi/GetLogicalDriveStringsW, fs.getlogicaldrivestrings, winbase/GetLogicalDriveStrings, winbase/GetLogicalDriveStringsA, winbase/GetLogicalDriveStringsW
f1_keywords:
- winbase/GetLogicalDriveStrings
dev_langs:
- c++
req.header: winbase.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetLogicalDriveStringsA function


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
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



Each string in the buffer may be used wherever a root directory is required, such as for the 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdrivetypea">GetDriveType</a> and 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a> functions.

This function returns a concatenation of the drives in the Global and Local MS-DOS Device namespaces. If a 
    drive exists in both namespaces, this function will return the entry in the Local MS-DOS Device namespace. For 
    more information, see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS DOS Device Name</a>.

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
     <a href="https://docs.microsoft.com/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle">Obtaining a File Name From a File Handle</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdrivetypea">GetDriveType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
 

 

