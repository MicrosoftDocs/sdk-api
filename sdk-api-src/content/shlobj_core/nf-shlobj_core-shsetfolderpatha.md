---
UID: NF:shlobj_core.SHSetFolderPathA
title: SHSetFolderPathA function (shlobj_core.h)
description: Deprecated. Assigns a new path to a system folder identified by its CSIDL. (ANSI)
helpviewer_keywords: ["SHSetFolderPathA", "shlobj_core/SHSetFolderPathA"]
old-location: shell\SHSetFolderPath.htm
tech.root: shell
ms.assetid: 9da142fa-4765-4889-bd4c-d8167a16f86b
ms.date: 12/05/2018
ms.keywords: SHSetFolderPath, SHSetFolderPath function [Windows Shell], SHSetFolderPathA, SHSetFolderPathW, _win32_SHSetFolderPath, shell.SHSetFolderPath, shlobj_core/SHSetFolderPath, shlobj_core/SHSetFolderPathA, shlobj_core/SHSetFolderPathW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHSetFolderPathW (Unicode) and SHSetFolderPathA (ANSI)
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
 - SHSetFolderPathA
 - shlobj_core/SHSetFolderPathA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHSetFolderPath
 - SHSetFolderPathA
 - SHSetFolderPathW
---

# SHSetFolderPathA function


## -description

Deprecated. Assigns a new path to a system folder identified by its CSIDL.

## -parameters

### -param csidl [in]

Type: <b>int</b>

A <a href="/windows/desktop/shell/csidl">CSIDL</a> value that identifies the folder whose path is to be set. Only physical folders are valid. If a virtual folder is specified, this function fails.

Add the <a href="/windows/desktop/shell/csidl">CSIDL_FLAG_DONT_UNEXPAND</a> value to the CSIDL to ensure that the string is written to the registry exactly as provided. If the <a href="/windows/desktop/shell/csidl">CSIDL_FLAG_DONT_UNEXPAND</a> flag is not included, portions of the path may be replaced by environment strings, such as %USERPROFILE%.

### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> that can be used to represent a particular user. This parameter is usually set to <b>NULL</b>, in which case the function tries to access the current user's instance of the folder. However, you may need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <b>Documents</b>.

The calling application is responsible for correct impersonation when <i>hToken</i> is non-null. It must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. See <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> for further discussion of access control issues.

### -param dwFlags [in]

Type: <b>DWORD</b>

Reserved. Must be set to 0.

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the folder's new path. This value cannot be <b>NULL</b>, and the string cannot be of zero length.

## -returns

Type: <b>HRESULT</b>

Returns standard <b>HRESULT</b> codes, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The folder's path was successfully updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Several error conditions cause the return of this value, including the following:

<ul>
<li>The <i>csidl</i> value is not valid.</li>
<li>The <i>csidl</i> value does not refer to a virtual folder.</li>
<li>The <i>csidl</i> value does not refer to a system folder.</li>
<li>The <i>csidl</i> value refers to a folder that cannot be renamed or moved.</li>
<li>The <i>dwFlags</i> value is not 0 (zero).</li>
<li>The <i>pszPath</i> value is <b>NULL</b>.</li>
<li>The string pointed to by <i>pszPath</i> value is an empty string ("") of length zero.</li>
</ul>
</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  As of Windows Vista, this function is merely a wrapper for <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a>. The CSIDL value is translated to its associated <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> and <b>SHSetKnownFolderPath</b> is called. New applications should use the known folder system rather than the older CSIDL system, which is supported only for backward compatibility.</div>
<div> </div>
<b>SHSetFolderPath</b> is not exported by name from Shell32.dll. To use the function, you must call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> with ordinal 231 for <b>SHSetFolderPathA</b> (for ANSI strings) or ordinal 232 for <b>SHSetFolderPathW</b> (for Unicode strings) to obtain a function pointer.

It is recommended that the paths be expressed as Unicode strings because folder names might contain Unicode characters not expressible in ANSI.





> [!NOTE]
> The shlobj_core.h header defines SHSetFolderPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath">IKnownFolder::SetPath</a>
