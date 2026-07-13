---
UID: NF:shlwapi.StrCmpNICW
title: StrCmpNICW function (shlwapi.h)
description: Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive. (Unicode)
helpviewer_keywords: ["StrCmpNIC", "StrCmpNIC function [Windows Shell]", "StrCmpNICW", "_shell_StrCmpNIC", "shell.StrCmpNIC", "shlwapi/StrCmpNIC", "shlwapi/StrCmpNICW"]
old-location: shell\StrCmpNIC.htm
tech.root: shell
ms.assetid: ed2e7df9-7f36-4566-8a3e-e3517307a584
ms.date: 12/05/2018
ms.keywords: StrCmpNIC, StrCmpNIC function [Windows Shell], StrCmpNICA, StrCmpNICW, _shell_StrCmpNIC, shell.StrCmpNIC, shlwapi/StrCmpNIC, shlwapi/StrCmpNICA, shlwapi/StrCmpNICW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpNICW (Unicode) and StrCmpNICA (ANSI)
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
 - StrCmpNICW
 - shlwapi/StrCmpNICW
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
 - StrCmpNIC
 - StrCmpNICA
 - StrCmpNICW
---

# StrCmpNICW function


## -description

Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules. The comparison is not case-sensitive.

## -parameters

### -param pszStr1 [in]

Type: <b>LPCTSTR</b>

A pointer to the first null-terminated string to be compared.

### -param pszStr2 [in]

Type: <b>LPCTSTR</b>

A pointer to the second null-terminated string to be compared.

### -param nChar

Type: <b>int</b>

The number of characters from the beginning of each string to be compared.

## -returns

Type: <b>int</b>

Returns zero if the substrings are identical. Returns a positive value if the string taken from that pointed to by <i>pszStr1</i> is alphabetically greater the string taken from that pointed to by <i>pszStr2</i>. Returns a negative value if the string taken from that pointed to by <i>pszStr1</i> is alphabetically less than the string taken from that pointed to by <i>pszStr2</i>.

## -remarks

Note that <b>StrCmpNIC</b> was designed for comparing canonical strings. These strings are not localized and consist only of characters below ASCII value 128. Therefore, it will not function correctly with a double-byte character set (DBCS) or other multiple-character data.

This function locates the first unequal characters and returns a positive number if the character from the first string is greater than the character from the second, a negative number if it is less, or zero if they are equal. For example, suppose that <i>pszStr1</i>="abczb", <i>pszStr2</i>="abcdefg", and you are comparing the first four characters from each. <b>StrCmpNIC</b> determines that the first unequal character is at position four ("z" in <i>pszStr1</i> and "d" in <i>pszStr2</i>) and returns a positive value since the ASCII code for "z" is greater than the ASCII code for "d".

For those versions of Windows that do not include <b>StrCmpNIC</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>StrCmpNICA</b> is ordinal 153 and <b>StrCmpNICW</b> is ordinal 154.





> [!NOTE]
> The shlwapi.h header defines StrCmpNIC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strcmpica">StrCmpIC</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strcmpnia">StrCmpNI</a>
