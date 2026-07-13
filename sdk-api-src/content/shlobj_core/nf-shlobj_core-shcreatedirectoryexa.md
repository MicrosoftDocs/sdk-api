---
UID: NF:shlobj_core.SHCreateDirectoryExA
title: SHCreateDirectoryExA function (shlobj_core.h)
description: Creates a new file system folder, with optional security attributes. (ANSI)
helpviewer_keywords: ["SHCreateDirectoryExA", "shlobj_core/SHCreateDirectoryExA"]
old-location: shell\SHCreateDirectoryEx.htm
tech.root: shell
ms.assetid: 7f44f907-cd12-4156-91c0-76e577ae25f6
ms.date: 12/05/2018
ms.keywords: SHCreateDirectoryEx, SHCreateDirectoryEx function [Windows Shell], SHCreateDirectoryExA, SHCreateDirectoryExW, _win32_SHCreateDirectoryEx, shell.SHCreateDirectoryEx, shlobj_core/SHCreateDirectoryEx, shlobj_core/SHCreateDirectoryExA, shlobj_core/SHCreateDirectoryExW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHCreateDirectoryExW (Unicode) and SHCreateDirectoryExA (ANSI)
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
 - SHCreateDirectoryExA
 - shlobj_core/SHCreateDirectoryExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHCreateDirectoryEx
 - SHCreateDirectoryExA
 - SHCreateDirectoryExW
---

# SHCreateDirectoryExA function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Creates a new file system folder, with optional security attributes.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to a parent window. This parameter can be set to <b>NULL</b> if no user interface will be displayed.

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string specifying the fully qualified path of the directory. This string is of maximum length of 248 characters, including the terminating null character.

### -param psa [in, optional]

Type: <b>const <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>*</b>

 A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure with the directory's security attribute. Set this parameter to <b>NULL</b> if no security attributes need to be set.

## -returns

Type: <b>int</b>

Returns <b>ERROR_SUCCESS</b> if successful. If the operation fails, other error codes can be returned, including those listed here. For values not specifically listed, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

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
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the path pointed to by <i>pszPath</i>. The path may contain an invalid entry.

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

This function creates a file system folder whose fully qualified path is given by <i>pszPath</i>. If one or more of the intermediate folders do not exist, they are created as well. <b>SHCreateDirectoryEx</b> also verifies that the files are visible. If they are not visible, expect one of the following:

				

<ul>
<li>If <i>hwnd</i> is set to a valid window handle, a message box is displayed warning the user that he or she might not be able to access the files. If the user chooses not to proceed, the function returns <b>ERROR_CANCELLED</b>.</li>
<li>If <i>hwnd</i> is set to <b>NULL</b>, no user interface is displayed and the function returns <b>ERROR_CANCELLED</b>.</li>
</ul>




> [!NOTE]
> The shlobj_core.h header defines SHCreateDirectoryEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedirectory">SHCreateDirectory</a>
