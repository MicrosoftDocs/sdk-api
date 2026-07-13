---
UID: NF:shlobj_core.PathCleanupSpec
title: PathCleanupSpec function (shlobj_core.h)
description: PathCleanupSpec may be altered or unavailable.
helpviewer_keywords: ["PathCleanupSpec","PathCleanupSpec function [Windows Shell]","_win32_PathCleanupSpec","shell.PathCleanupSpec","shlobj_core/PathCleanupSpec"]
old-location: shell\PathCleanupSpec.htm
tech.root: shell
ms.assetid: 593fd2b7-44ae-4309-a185-97e42f3cc0fa
ms.date: 12/05/2018
ms.keywords: PathCleanupSpec, PathCleanupSpec function [Windows Shell], _win32_PathCleanupSpec, shell.PathCleanupSpec, shlobj_core/PathCleanupSpec
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathCleanupSpec
 - shlobj_core/PathCleanupSpec
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - PathCleanupSpec
---

# PathCleanupSpec function


## -description

<p class="CCE_Message">[<b>PathCleanupSpec</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes illegal characters from a file or directory name. Enforces the 8.3 filename format on drives that do not support long file names.

## -parameters

### -param pszDir [in, optional]

Type: <b>PCWSTR</b>

A pointer to a null-terminated buffer that contains the fully qualified path of the directory that will contain the file or directory named at <i>pszSpec</i>. The path must not exceed MAX_PATH characters in length, including the terminating null character. This path is not altered.
                        
                        

This value can be <b>NULL</b>.

### -param pszSpec [in, out]

Type: <b>PWSTR</b>

A pointer to a null-terminated buffer that contains the file or directory name to be cleaned. In the case of a file, include the file's extension. Note that because '\' is considered an invalid character and will be removed, this buffer cannot contain a path more than one directory deep.
                    
                        

On exit, the buffer contains a null-terminated string that includes the cleaned name.

This buffer should be at least MAX_PATH characters in length to avoid the possibility of a buffer overrun.

## -returns

Type: <b>int</b>

Returns one or more of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PCS_REPLACEDCHAR</b></dt>
</dl>
</td>
<td width="60%">
Replaced one or more invalid characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PCS_REMOVEDCHAR</b></dt>
</dl>
</td>
<td width="60%">
Removed one or more invalid characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PCS_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The returned path is truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PCS_PATHTOOLONG</b></dt>
</dl>
</td>
<td width="60%">
The function failed because the input path specified at <i>pszDir</i> is too long to allow the formation of a valid file name from <i>pszSpec</i>. When this flag is returned, it is always accompanied by the PCS_FATAL flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PCS_FATAL</b></dt>
</dl>
</td>
<td width="60%">
The cleaned path is not a valid file name. This flag is always returned in conjunction with PCS_PATHTOOLONG.

</td>
</tr>
</table>

## -remarks

The following are considered invalid characters in all names.
                


```
\ / : * ? " < > |
```


Control characters are also considered invalid. If long file names are not supported, the semi-colon (;) and comma (,) characters are also invalid.

The drive named in <i>pszDir</i> is checked to determine 
whether its file system supports long file names. If it does not, the name at <i>pszSpec</i> is truncated to the 8.3 format and the PCS_TRUNCATED value returned. If <i>pszDir</i> is <b>NULL</b>, the drive on which Windows is installed is used to determine long file name support.

If the full path—the number of characters in the path at <i>pszDir</i> plus the number of characters in the cleaned name at <i>pszSpec</i>—exceeds MAX_PATH – 1 (to account for the terminating null character), the function returns PCS_PATHTOOLONG.

