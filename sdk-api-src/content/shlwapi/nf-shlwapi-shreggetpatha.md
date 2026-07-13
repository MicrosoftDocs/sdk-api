---
UID: NF:shlwapi.SHRegGetPathA
title: SHRegGetPathA function (shlwapi.h)
description: Retrieves a file path from the registry, expanding environment variables as needed. (ANSI)
helpviewer_keywords: ["SHRegGetPathA", "shlwapi/SHRegGetPathA"]
old-location: shell\SHRegGetPath.htm
tech.root: shell
ms.assetid: 2874b868-33f9-4f20-9e0b-136125cf268c
ms.date: 12/05/2018
ms.keywords: SHRegGetPath, SHRegGetPath function [Windows Shell], SHRegGetPathA, SHRegGetPathW, _win32_SHRegGetPath, shell.SHRegGetPath, shlwapi/SHRegGetPath, shlwapi/SHRegGetPathA, shlwapi/SHRegGetPathW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegGetPathW (Unicode) and SHRegGetPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRegGetPathA
 - shlwapi/SHRegGetPathA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-Registry-l1-1-0.dll
 - API-MS-Win-ShCore-Registry-l1-1-1.dll
api_name:
 - SHRegGetPath
 - SHRegGetPathA
 - SHRegGetPathW
---

# SHRegGetPathA function


## -description

Retrieves a file path from the registry, expanding environment variables as needed.

## -parameters

### -param hKey [in]

Type: <b>HKEY</b>

A handle to a key that is currently open, or a registry root key.

### -param pcszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the name of the subkey.

### -param pcszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the name of the value that holds the unexpanded path string.

### -param pszPath [out]

Type: <b>LPTSTR</b>

A buffer to hold the expanded path. You should set the size of this buffer to <b>MAX_PATH</b> to ensure that it is large enough to hold the returned string.

### -param dwFlags

Type: <b>DWORD</b>

Reserved.

## -returns

Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a Windows error code otherwise.

## -remarks

The data type of the specified registry value must be either <b>REG_EXPAND_SZ</b> or <b>REG_SZ</b>. If it has the <b>REG_EXPAND_SZ</b> type, any environment variables in the registry string will be expanded with <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">ExpandEnvironmentStrings</a>. If it has the <b>REG_SZ</b> data type, environment variables will not be expanded and the string pointed to by <i>pszPath</i> will be identical to the string in the registry.

The following environment strings will be replaced by their equivalent path.

<table class="clsStd">
<tr>
<th>Environment string</th>
<th>Folder</th>
</tr>
<tr>
<td>%USERPROFILE%
						</td>
<td>The current user's profile folder</td>
</tr>
<tr>
<td>%ALLUSERSPROFILE%
						</td>
<td>The All Users profile folder</td>
</tr>
<tr>
<td>%ProgramFiles%
						</td>
<td>The Program Files folder</td>
</tr>
<tr>
<td>%SystemRoot%
						</td>
<td>The system root folder</td>
</tr>
<tr>
<td>%SystemDrive%
						</td>
<td>The system drive letter</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  %USERPROFILE% is relative to the user making the call. This function does not work if the user is being impersonated from a service.</div>
<div> </div>



> [!NOTE]
> The shlwapi.h header defines SHRegGetPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
