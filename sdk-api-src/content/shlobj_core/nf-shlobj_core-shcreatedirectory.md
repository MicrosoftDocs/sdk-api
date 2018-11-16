---
UID: NF:shlobj_core.SHCreateDirectory
title: SHCreateDirectory function
author: windows-sdk-content
description: Creates a new file system folder.
old-location: shell\SHCreateDirectory.htm
tech.root: shell
ms.assetid: 4927429c-f457-4dda-aa0d-236eb236795c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SHCreateDirectory, SHCreateDirectory function [Windows Shell], _win32_SHCreateDirectory, shell.SHCreateDirectory, shlobj_core/SHCreateDirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreateDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SHCreateDirectory
: 
---

# SHCreateDirectory function


## -description


<p class="CCE_Message">[<b>SHCreateDirectory</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a new file system folder.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to a parent window. This parameter can be set to <b>NULL</b> if no user interface is displayed.


### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that contains the fully qualified path of the directory. This string should have no more than MAX_PATH characters, including the terminating null character.


## -returns



Type: <b>int</b>

Returns <b>ERROR_SUCCESS</b> if successful. If the operation fails, other error codes can be returned, including those listed here. For values not specifically listed, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszPath</i> parameter was set to a relative path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILENAME_EXCED_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The path pointed to by <i>pszPath</i> is too long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The directory exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The directory exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation.

</td>
</tr>
</table>
 




## -remarks



This function creates a file system folder whose fully qualified path is given by <i>pszPath</i>. If one or more of the intermediate folders do not exist, it creates them.

To set security attributes on a new folder, use <a href="https://msdn.microsoft.com/7f44f907-cd12-4156-91c0-76e577ae25f6">SHCreateDirectoryEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/7f44f907-cd12-4156-91c0-76e577ae25f6">SHCreateDirectoryEx</a>
 

 

