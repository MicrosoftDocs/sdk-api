---
UID: NF:shlwapi.PathMatchSpecExA
title: PathMatchSpecExA function (shlwapi.h)
description: Matches a file name from a path against one or more file name patterns. (ANSI)
helpviewer_keywords: ["PMSF_DONT_STRIP_SPACES", "PMSF_MULTIPLE", "PMSF_NORMAL", "PathMatchSpecExA", "shlwapi/PathMatchSpecExA"]
old-location: shell\PathMatchSpecEx.htm
tech.root: shell
ms.assetid: bd9bf950-e349-4b67-8608-7acad84c0907
ms.date: 12/05/2018
ms.keywords: PMSF_DONT_STRIP_SPACES, PMSF_MULTIPLE, PMSF_NORMAL, PathMatchSpecEx, PathMatchSpecEx function [Windows Shell], PathMatchSpecExA, PathMatchSpecExW, _win32_PathMatchSpecEx, shell.PathMatchSpecEx, shlwapi/PathMatchSpecEx, shlwapi/PathMatchSpecExA, shlwapi/PathMatchSpecExW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathMatchSpecExW (Unicode) and PathMatchSpecExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 7.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathMatchSpecExA
 - shlwapi/PathMatchSpecExA
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
 - PathMatchSpecEx
 - PathMatchSpecExA
 - PathMatchSpecExW
---

# PathMatchSpecExA function


## -description

Matches a file name from a path against one or more file name patterns.

## -parameters

### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the path from which the file name to be matched is taken.

### -param pszSpec [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the file name pattern for which to search. This can be the exact name, or it can contain wildcard characters. If exactly one pattern is specified, set the <b>PMSF_NORMAL</b> flag in <i>dwFlags</i>. If more than one pattern is specified, separate them with semicolons and set the <b>PMSF_MULTIPLE</b> flag.

### -param dwFlags [in]

Type: <b>DWORD</b>

Modifies the search condition. The following are valid flags.



#### PMSF_NORMAL (0x00000000)

The <i>pszSpec</i> parameter points to a single file name pattern to be matched.



#### PMSF_MULTIPLE (0x00000001)

The <i>pszSpec</i> parameter points to a semicolon-delimited list of file name patterns to be matched.



#### PMSF_DONT_STRIP_SPACES (0x00010000)

If <b>PMSF_NORMAL</b> is used, don't ignore leading spaces in the string pointed to by <i>pszSpec</i>. If <b>PMSF_MULTIPLE</b> is used, don't ignore leading spaces in each file type contained in the string pointed to by <i>pszSpec</i>. This flag can be combined with <b>PMSF_NORMAL</b> and <b>PMSF_MULTIPLE</b>.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

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
A file name pattern specified in <i>pszSpec</i> matched the file name found in the string pointed to by <i>pszFile</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No file name pattern specified in <i>pszSpec</i> matched the file name found in the string pointed to by <i>pszFile</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathmatchspeca">PathMatchSpec</a>

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathMatchSpecEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
