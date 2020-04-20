---
UID: NF:shlwapi.StrCmpCA
title: StrCmpCA function (shlwapi.h)
description: Compares strings using C run-time (ASCII) collation rules. The comparison is case-sensitive.helpviewer_keywords: ["StrCmpC","StrCmpC function [Windows Shell]","StrCmpCA","StrCmpCW","_shell_StrCmpC","shell.StrCmpC","shlwapi/StrCmpC","shlwapi/StrCmpCA","shlwapi/StrCmpCW"]
old-location: shell\StrCmpC.htm
tech.root: shell
ms.assetid: f4c4bc76-1e42-4cb0-bf74-d395743c9b1c
ms.date: 12/05/2018
ms.keywords: StrCmpC, StrCmpC function [Windows Shell], StrCmpCA, StrCmpCW, _shell_StrCmpC, shell.StrCmpC, shlwapi/StrCmpC, shlwapi/StrCmpCA, shlwapi/StrCmpCW
f1_keywords:
- shlwapi/StrCmpC
dev_langs:
- c++
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpCW (Unicode) and StrCmpCA (ANSI)
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
- API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
- API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
- StrCmpC
- StrCmpCA
- StrCmpCW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrCmpCA function


## -description


Compares strings using C run-time (ASCII) collation rules. The comparison is case-sensitive.


## -parameters




### -param pszStr1 [out]

Type: <b>LPCTSTR</b>

A pointer to the first null-terminated string to be compared.


### -param pszStr2 [out]

Type: <b>LPCTSTR</b>

A pointer to the second null-terminated string to be compared.


## -returns



Type: <b>int</b>

Returns zero if the strings are identical. Returns a positive value if the string pointed to by <i>lpStr1</i> is alphabetically greater than that pointed to by <i>lpStr2</i>. Returns a negative value if the string pointed to by <i>lpStr1</i> is alphabetically less than that pointed to by <i>lpStr2</i>.




## -remarks



It is strongly recommended that you use the <a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> function in place of this function. <b>StrCmpC</b> was designed for comparing canonical strings. These strings are not localized and consist only of characters below ASCII value 128. Therefore, it will not function correctly with a double-byte character set (DBCS) or other multiple-character data.

This function locates the first unequal characters and returns a positive number if the character from the first string is greater than the character from the second, a negative number if it is less, or zero if they are equal. For example, if <i>lpStr1</i>="abczb" and <i>lpStr2</i>="abcdefg", <b>StrCmpC</b> determines that the first unequal character is at position four ("z" in <i>lpStr1</i> and "d" in <i>lpStr2</i>) and returns a positive value since the ASCII code for "z" is greater than the ASCII code for "d".

For those versions of Windows that do not include <b>StrCmpC</b> in Shlwapi.h, this function's individual ANSI or Unicode version must be called directly from Shlwapi.dll. <b>StrCmpCA</b> is ordinal 155 and <b>StrCmpCW</b> is ordinal 156.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a>
 

 

