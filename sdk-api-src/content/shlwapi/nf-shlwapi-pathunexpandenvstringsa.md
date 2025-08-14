---
UID: NF:shlwapi.PathUnExpandEnvStringsA
title: PathUnExpandEnvStringsA function (shlwapi.h)
description: Replaces certain folder names in a fully qualified path with their associated environment string. (ANSI)
helpviewer_keywords: ["PathUnExpandEnvStringsA", "shlwapi/PathUnExpandEnvStringsA"]
old-location: shell\PathUnExpandEnvStrings.htm
tech.root: shell
ms.assetid: cfab1ee0-03f3-4e0f-a29d-5331fec022b5
ms.date: 12/05/2018
ms.keywords: PathUnExpandEnvStrings, PathUnExpandEnvStrings function [Windows Shell], PathUnExpandEnvStringsA, PathUnExpandEnvStringsW, _win32_PathUnExpandEnvStrings, shell.PathUnExpandEnvStrings, shlwapi/PathUnExpandEnvStrings, shlwapi/PathUnExpandEnvStringsA, shlwapi/PathUnExpandEnvStringsW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathUnExpandEnvStringsW (Unicode) and PathUnExpandEnvStringsA (ANSI)
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
 - PathUnExpandEnvStringsA
 - shlwapi/PathUnExpandEnvStringsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l1-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathUnExpandEnvStrings
 - PathUnExpandEnvStringsA
 - PathUnExpandEnvStringsW
---

# PathUnExpandEnvStringsA function


## -description

Replaces certain folder names in a fully qualified path with their associated environment string.

## -parameters

### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be unexpanded.

### -param pszBuf [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this method returns successfully, receives the unexpanded string. The size of this buffer must be set to MAX_PATH to ensure that it is large enough to hold the returned string.

### -param cchBuf [in]

Type: <b>UINT</b>

The size, in characters, in the <i>pszBuf</i> buffer.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

The following folder paths are replaced by their equivalent environment string.

<table class="clsStd">
<tr>
<th>Folder</th>
<th>Environment String</th>
</tr>
<tr>
<td>The All Users profile folder</td>
<td>%ALLUSERSPROFILE%</td>
</tr>
<tr>
<td>The current user's application data folder (Windows Vista and later only).</td>
<td>%APPDATA%</td>
</tr>
<tr>
<td>The system name</td>
<td>%COMPUTERNAME%</td>
</tr>
<tr>
<td>The Program Files folder</td>
<td>%ProgramFiles%</td>
</tr>
<tr>
<td>The system root folder</td>
<td>%SystemRoot%</td>
</tr>
<tr>
<td>The system drive letter</td>
<td>%SystemDrive%</td>
</tr>
<tr>
<td>The current user's profile folder</td>
<td>%USERPROFILE%</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  %APPDATA% and %USERPROFILE% are relative to the user making the call. This function does not work if the user is being impersonated from a service. For further discussion of access control issues, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>.</div>
<div> </div>
The environment variables listed in the above table might not all be set on all systems. If an environment variable is not set, it is not unexpanded.





> [!NOTE]
> The shlwapi.h header defines PathUnExpandEnvStrings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shellapi/nf-shellapi-doenvironmentsubsta">DoEnvironmentSubst</a>
