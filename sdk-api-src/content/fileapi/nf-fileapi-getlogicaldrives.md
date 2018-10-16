---
UID: NF:fileapi.GetLogicalDrives
title: GetLogicalDrives function
author: windows-sdk-content
description: Retrieves a bitmask representing the currently available disk drives.
old-location: fs\getlogicaldrives.htm
tech.root: fileio
ms.assetid: 21a66050-3bab-4c70-9003-3b52e8c72b00
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetLogicalDrives, GetLogicalDrives function [Files], _win32_getlogicaldrives, base.getlogicaldrives, fileapi/GetLogicalDrives, fs.getlogicaldrives, winbase/GetLogicalDrives
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - GetLogicalDrives
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLogicalDrives function


## -description


Retrieves a bitmask representing the currently available disk drives.


## -parameters






## -returns



If the function succeeds, the return value is a bitmask representing the currently available disk drives. Bit position 0 (the least-significant bit) is drive A, bit position 1 is drive B, bit position 2 is drive C, and so on.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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




<a href="https://msdn.microsoft.com/d3a83f8d-c37c-48b9-a24c-f81dfe5773e9">GetLogicalDriveStrings</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

