---
UID: NF:shlwapi.StrCmpICW
title: StrCmpICW function (shlwapi.h)
description: Compares two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive. (Unicode)
helpviewer_keywords: ["StrCmpIC","StrCmpIC function [Windows Shell]","StrCmpICA","StrCmpICW","_shell_StrCmpIC","shell.StrCmpIC","shlwapi/StrCmpIC","shlwapi/StrCmpICA","shlwapi/StrCmpICW"]
old-location: shell\StrCmpIC.htm
tech.root: shell
ms.assetid: 3f6d1ca1-fbd2-4ce2-b6d4-c3dfb37f1f87
ms.date: 12/05/2018
ms.keywords: StrCmpIC, StrCmpIC function [Windows Shell], StrCmpICA, StrCmpICW, _shell_StrCmpIC, shell.StrCmpIC, shlwapi/StrCmpIC, shlwapi/StrCmpICA, shlwapi/StrCmpICW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpICW (Unicode) and StrCmpICA (ANSI)
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
 - StrCmpICW
 - shlwapi/StrCmpICW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrCmpIC
 - StrCmpICA
 - StrCmpICW
---

# StrCmpICW function


## -description

Compares two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive.

## -parameters

### -param pszStr1 [in]

Type: <b>LPCTSTR</b>

A pointer to the first null-terminated string to be compared.

### -param pszStr2 [in]

Type: <b>LPCTSTR</b>

A pointer to the second null-terminated string to be compared.

## -returns

Type: <b>int</b>

Returns zero if the strings are identical. Returns a positive value if the string pointed to by <i>lpStr1</i> is alphabetically greater than that pointed to by <i>lpStr2</i>. Returns a negative value if the string pointed to by <i>lpStr1</i> is alphabetically less than that pointed to by <i>lpStr2</i>

## -remarks

It is strongly recommended that you use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> in place of this function. <b>StrCmpIC</b> was designed for comparing canonical strings. These strings are not localized and consist only of characters below ASCII value 128. Therefore, it will not function correctly with double-byte character set (DBCS) data.

Uppercase characters are converted to lowercase characters before comparing, and the return value is based on comparing the converted values.  This function returns the difference in value of the first unequal characters it encounters, or zero if they are all equal. For example, if <i>lpStr1</i>="abczb" and <i>lpStr2</i>="abcdefg", <b>StrCmpIC</b> determines that "abczb" is greater than "abcdefg" and returns z - d.

For those versions of Windows that do not include <b>StrCmpIC</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>StrCmpICA</b> is ordinal 157 and <b>StrCmpICW</b> is ordinal 158.





> [!NOTE]
> The shlwapi.h header defines StrCmpIC as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>
