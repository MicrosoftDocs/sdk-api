---
UID: NF:fileapi.GetLogicalDrives
title: GetLogicalDrives function (fileapi.h)
description: Retrieves a bitmask representing the currently available disk drives.
helpviewer_keywords: ["GetLogicalDrives","GetLogicalDrives function [Files]","_win32_getlogicaldrives","base.getlogicaldrives","fileapi/GetLogicalDrives","fs.getlogicaldrives","winbase/GetLogicalDrives"]
old-location: fs\getlogicaldrives.htm
tech.root: fs
ms.assetid: 21a66050-3bab-4c70-9003-3b52e8c72b00
ms.date: 12/05/2018
ms.keywords: GetLogicalDrives, GetLogicalDrives function [Files], _win32_getlogicaldrives, base.getlogicaldrives, fileapi/GetLogicalDrives, fs.getlogicaldrives, winbase/GetLogicalDrives
req.header: fileapi.h
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
 - GetLogicalDrives
 - fileapi/GetLogicalDrives
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
 - GetLogicalDrives
---

# GetLogicalDrives function


## -description

Retrieves a bitmask representing the currently available disk drives.



## -returns

If the function succeeds, the return value is a bitmask representing the currently available disk drives. Bit position 0 (the least-significant bit) is drive A, bit position 1 is drive B, bit position 2 is drive C, and so on.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

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

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrivestringsw">GetLogicalDriveStrings</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
