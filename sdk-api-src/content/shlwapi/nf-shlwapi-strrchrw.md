---
UID: NF:shlwapi.StrRChrW
title: StrRChrW function (shlwapi.h)
description: Searches a string for the last occurrence of a specified character. The comparison is case-sensitive.helpviewer_keywords: ["StrRChr","StrRChr function [Windows Shell]","StrRChrA","StrRChrW","_win32_StrRChr","shell.StrRChr","shlwapi/StrRChr","shlwapi/StrRChrA","shlwapi/StrRChrW"]
old-location: shell\StrRChr.htm
tech.root: shell
ms.assetid: 7f1e91ad-aaa0-4449-834e-8e309c88d6b1
ms.date: 12/05/2018
ms.keywords: StrRChr, StrRChr function [Windows Shell], StrRChrA, StrRChrW, _win32_StrRChr, shell.StrRChr, shlwapi/StrRChr, shlwapi/StrRChrA, shlwapi/StrRChrW
f1_keywords:
- shlwapi/StrRChr
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
req.unicode-ansi: StrRChrW (Unicode) and StrRChrA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
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
- StrRChr
- StrRChrA
- StrRChrW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrRChrW function


## -description


Searches a string for the last occurrence of a specified character. The comparison is case-sensitive.


## -parameters




### -param pszStart [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to be searched.


### -param pszEnd [in, optional]

Type: <b>PCTSTR</b>

A pointer into the source string that defines the range of the search. Set <i>pszEnd</i> to point to a character in the string and the search will stop with the preceding character. Set <i>pszEnd</i> to <b>NULL</b> to search the entire string.


### -param wMatch

Type: <b>TCHAR</b>

The character to search for.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to the last occurrence of the character in the string, if successful, or <b>NULL</b> if not.




## -remarks



The comparison assumes that <i>pszEnd</i> points to the end of the string.



