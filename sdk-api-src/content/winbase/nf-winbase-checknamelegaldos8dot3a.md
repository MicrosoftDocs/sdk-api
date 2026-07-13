---
UID: NF:winbase.CheckNameLegalDOS8Dot3A
title: CheckNameLegalDOS8Dot3A function (winbase.h)
description: Determines whether the specified name can be used to create a file on a FAT file system. (ANSI)
helpviewer_keywords: ["CheckNameLegalDOS8Dot3A", "winbase/CheckNameLegalDOS8Dot3A"]
old-location: fs\checknamelegaldos8dot3.htm
tech.root: fs
ms.assetid: bb0edcc5-4991-47d0-9ade-6c6776a36f39
ms.date: 12/05/2018
ms.keywords: CheckNameLegalDOS8Dot3, CheckNameLegalDOS8Dot3 function [Files], CheckNameLegalDOS8Dot3A, CheckNameLegalDOS8Dot3W, base.checknamelegaldos8dot3, fs.checknamelegaldos8dot3, winbase/CheckNameLegalDOS8Dot3, winbase/CheckNameLegalDOS8Dot3A, winbase/CheckNameLegalDOS8Dot3W
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CheckNameLegalDOS8Dot3A
 - winbase/CheckNameLegalDOS8Dot3A
dev_langs:
 - c++
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
---

# CheckNameLegalDOS8Dot3A function


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

### -param pbNameContainsSpaces [out, optional]

Indicates whether or not a name contains spaces. This parameter can be <b>NULL</b>. If 
      the name is not a valid 8.3 FAT file system name, this parameter is undefined.

### -param pbNameLegal [out]

If the function succeeds, this parameter indicates whether a file name is a valid 8.3 FAT file name when 
      the current OEM code page is applied to the file name.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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






> [!NOTE]
> The winbase.h header defines CheckNameLegalDOS8Dot3 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winnls/nf-winnls-getoemcp">GetOEMCP</a>
