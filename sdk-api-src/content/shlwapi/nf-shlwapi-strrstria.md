---
UID: NF:shlwapi.StrRStrIA
title: StrRStrIA function (shlwapi.h)
description: Searches for the last occurrence of a specified substring within a string. The comparison is not case-sensitive.helpviewer_keywords: ["StrRStrI","StrRStrI function [Windows Shell]","StrRStrIA","StrRStrIW","_win32_StrRStrI","shell.StrRStrI","shlwapi/StrRStrI","shlwapi/StrRStrIA","shlwapi/StrRStrIW"]
old-location: shell\StrRStrI.htm
tech.root: shell
ms.assetid: 41057976-6443-40dc-96f7-f2cbd5d494de
ms.date: 12/05/2018
ms.keywords: StrRStrI, StrRStrI function [Windows Shell], StrRStrIA, StrRStrIW, _win32_StrRStrI, shell.StrRStrI, shlwapi/StrRStrI, shlwapi/StrRStrIA, shlwapi/StrRStrIW
f1_keywords:
- shlwapi/StrRStrI
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
req.unicode-ansi: StrRStrIW (Unicode) and StrRStrIA (ANSI)
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
- StrRStrI
- StrRStrIA
- StrRStrIW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrRStrIA function


## -description


Searches for the last occurrence of a specified substring within a string. The comparison is not case-sensitive.


## -parameters




### -param pszSource [in]

Type: <b>PTSTR</b>

A pointer to a <b>null</b>-terminated source string.


### -param pszLast [in, optional]

Type: <b>PCTSTR</b>

A pointer into the source string that defines the range of the search. Set <i>pszLast</i> to point to a character in the source string, and the search will stop with the preceding character. Set <i>pszLast</i> to <b>NULL</b> to search the entire source string.


### -param pszSrch [in]

Type: <b>PCTSTR</b>

A pointer to the substring to search for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the last occurrence of the substring if successful, or <b>NULL</b> otherwise.



