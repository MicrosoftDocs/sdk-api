---
UID: NF:winbase.CheckNameLegalDOS8Dot3W
title: CheckNameLegalDOS8Dot3W function
author: windows-sdk-content
description: Determines whether the specified name can be used to create a file on a FAT file system.
old-location: fs\checknamelegaldos8dot3.htm
old-project: fileio
ms.assetid: bb0edcc5-4991-47d0-9ade-6c6776a36f39
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: CheckNameLegalDOS8Dot3, CheckNameLegalDOS8Dot3 function [Files], CheckNameLegalDOS8Dot3A, CheckNameLegalDOS8Dot3W, base.checknamelegaldos8dot3, fs.checknamelegaldos8dot3, winbase/CheckNameLegalDOS8Dot3, winbase/CheckNameLegalDOS8Dot3A, winbase/CheckNameLegalDOS8Dot3W
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CheckNameLegalDOS8Dot3W (Unicode) and CheckNameLegalDOS8Dot3A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - CheckNameLegalDOS8Dot3
 - CheckNameLegalDOS8Dot3A
 - CheckNameLegalDOS8Dot3W
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CheckNameLegalDOS8Dot3W function


## -description


Determines whether the  specified name can be used to create a file on a FAT file 
   system.


## -parameters




### -param lpName [in]

The file name, in 8.3 format.


### -param lpOemName [out, optional]

A pointer to a buffer that receives the OEM string that corresponds to <i>Name</i>. This 
      parameter can be <b>NULL</b>.


### -param OemNameSize [in]

The size of the <i>lpOemName</i> buffer, in characters. If 
      <i>lpOemName</i> is <b>NULL</b>, this parameter must be 0 (zero).


### -param OPTIONAL

TBD


### -param pbNameLegal [out]

If the function succeeds, this parameter indicates whether a file name is a valid 8.3 FAT file name when 
      the current OEM code page is applied to the file name.


#### - pbNameContainsSpaces [out, optional]

Indicates whether or not a name contains spaces. This parameter can be <b>NULL</b>. If 
      the name is not a valid 8.3 FAT file system name, this parameter is undefined.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function can be used to determine whether or not a file name can be passed to a 16-bit Windows-based 
    application or an MS-DOS-based application.

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
See remarks

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
See remarks

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
 

Note that SMB 3.0 does not support short names on shares with continuous availability capability, so function will always return zero (fail).





## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/e6d42641-4bbe-44d8-baea-1087e48dae7d">GetOEMCP</a>
 

 

