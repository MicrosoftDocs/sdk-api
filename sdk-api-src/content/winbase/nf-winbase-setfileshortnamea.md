---
UID: NF:winbase.SetFileShortNameA
title: SetFileShortNameA function
author: windows-sdk-content
description: Sets the short name for the specified file.
old-location: fs\setfileshortname.htm
tech.root: fileio
ms.assetid: 0f4beb95-4e6c-422e-a17c-3371b706f0d4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetFileShortName, SetFileShortName function [Files], SetFileShortNameA, SetFileShortNameW, _win32_setfileshortname, base.setfileshortname, fs.setfileshortname, winbase/SetFileShortName, winbase/SetFileShortNameA, winbase/SetFileShortNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetFileShortNameW (Unicode) and SetFileShortNameA (ANSI)
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
api_name:
 - SetFileShortName
 - SetFileShortNameA
 - SetFileShortNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetFileShortNameA function


## -description


Sets the short name for the specified file. The file must be on an NTFS file system 
    volume.


## -parameters




### -param hFile [in]

A handle to the file. The file must be opened with either the <b>GENERIC_ALL</b> access 
       right or <b>GENERIC_WRITE</b>|<b>DELETE</b>, and with the 
       <b>FILE_FLAG_BACKUP_SEMANTICS</b> file attribute.


### -param lpShortName [in]

A pointer to a string that specifies the short name for the file.

 Specifying  an empty (zero-length) string will remove the short file name, if it exists for the file specified by the <i>hFile</i> parameter. If  a short file name does not exist, the function will do nothing and return success.


<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This behavior is not supported. The parameter must contain a valid string of one or more characters.




## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 
      <b>GetLastError</b> may return one of the following error 
       codes that are specific to this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified short name is not unique.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either the specified file has been opened in case-sensitive mode or the specified short name is invalid.

</td>
</tr>
</table>
 




## -remarks



The caller of this function must have the <b>SE_RESTORE_NAME</b> privilege. For more 
    information, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

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
No

</td>
</tr>
</table>
 

SMB 3.0 does not support short names on shares with continuous availability capability . Short names are not recommended on CsvFs.





## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>
 

 

