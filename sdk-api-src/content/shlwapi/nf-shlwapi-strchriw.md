---
UID: NF:shlwapi.StrChrIW
title: StrChrIW function (shlwapi.h)
description: Searches a string for the first occurrence of a character that matches the specified character. The comparison is not case-sensitive.helpviewer_keywords: ["StrChrI","StrChrI function [Windows Shell]","StrChrIA","StrChrIW","_win32_StrChrI","shell.StrChrI","shlwapi/StrChrI","shlwapi/StrChrIA","shlwapi/StrChrIW"]
old-location: shell\StrChrI.htm
tech.root: shell
ms.assetid: bad606d2-e337-42b5-853e-c7afa8d3d71b
ms.date: 12/05/2018
ms.keywords: StrChrI, StrChrI function [Windows Shell], StrChrIA, StrChrIW, _win32_StrChrI, shell.StrChrI, shlwapi/StrChrI, shlwapi/StrChrIA, shlwapi/StrChrIW
f1_keywords:
- shlwapi/StrChrI
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
req.unicode-ansi: StrChrIW (Unicode) and StrChrIA (ANSI)
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
- StrChrI
- StrChrIA
- StrChrIW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrChrIW function


## -description


Searches a string for the first occurrence of a character that matches the specified character. The comparison is not case-sensitive.


## -parameters




### -param pszStart [in]

Type: <b>PTSTR</b>

A pointer to the string to be searched.


### -param wMatch

Type: <b>TCHAR</b>

The character to be used for comparison.


## -returns



Type: <b>PTSTR</b>

Returns the address of the first occurrence of the character in the string if successful, or <b>NULL</b> otherwise.




## -remarks



The comparison assumes <i>pszStart</i> points to the start of a null-terminated string.



