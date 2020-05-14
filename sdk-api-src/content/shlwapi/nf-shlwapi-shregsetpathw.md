---
UID: NF:shlwapi.SHRegSetPathW
title: SHRegSetPathW function (shlwapi.h)
description: Takes a file path, replaces folder names with environment strings, and places the resulting string in the registry.helpviewer_keywords: ["SHRegSetPath","SHRegSetPath function [Windows Shell]","SHRegSetPathA","SHRegSetPathW","_win32_SHRegSetPath","shell.SHRegSetPath","shlwapi/SHRegSetPath","shlwapi/SHRegSetPathA","shlwapi/SHRegSetPathW"]
old-location: shell\SHRegSetPath.htm
tech.root: shell
ms.assetid: 3ee6ec69-5d16-4bdd-a591-651af05bf944
ms.date: 12/05/2018
ms.keywords: SHRegSetPath, SHRegSetPath function [Windows Shell], SHRegSetPathA, SHRegSetPathW, _win32_SHRegSetPath, shell.SHRegSetPath, shlwapi/SHRegSetPath, shlwapi/SHRegSetPathA, shlwapi/SHRegSetPathW
f1_keywords:
- shlwapi/SHRegSetPath
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegSetPathW (Unicode) and SHRegSetPathA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
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
- SHRegSetPath
- SHRegSetPathA
- SHRegSetPathW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHRegSetPathW function


## -description


Takes a file path, replaces folder names with environment strings, and places the resulting string in the registry.


## -parameters




### -param hKey [in]

Type: <b>HKEY</b>

A handle to a key that is currently open, or a registry root key.


### -param pcszSubKey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string containing the name of an existing subkey. If the subkey does not exist, <b>SHRegSetPath</b> will fail.


### -param pcszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the value to hold the path string.


### -param pcszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with a fully qualified file path.


### -param dwFlags

Type: <b>DWORD</b>

Reserved.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a Windows error code otherwise.




## -remarks



For Windows 2000, <b>SHRegSetPath</b> uses <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-pathunexpandenvstringsa">PathUnExpandEnvStrings</a> to convert folder names to their corresponding environment string. If any environment variables were substituted, the registry value will be set with the <b>REG_EXPAND_SZ</b> data type. Otherwise, it will be set with the <b>REG_SZ</b> data type.

The following folder paths will be replaced by their equivalent environment string.

<table class="clsStd">
<tr>
<th>Folder</th>
<th>Environment string</th>
</tr>
<tr>
<td>The current user's profile folder</td>
<td>%USERPROFILE%
						</td>
</tr>
<tr>
<td>The All Users profile folder</td>
<td>%ALLUSERSPROFILE%
						</td>
</tr>
<tr>
<td>The Program Files folder</td>
<td>%ProgramFiles%
						</td>
</tr>
<tr>
<td>The system root folder</td>
<td>%SystemRoot%
						</td>
</tr>
<tr>
<td>The system drive letter</td>
<td>%SystemDrive%
						</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  %USERPROFILE% is relative to the user making the call. This function does not work if the user is being impersonated from a service.</div>
<div> </div>
The environment variables listed in the above table might not all be set on any particular system. If an environment variable is not set, it will not be unexpanded. In particular, none of these variables are set for the default environment of Windows 95 or Windows 98. The %ProgramFiles% variable is new for Windows 2000, and will typically not be set on Microsoft Windows NT 4.0 systems.



