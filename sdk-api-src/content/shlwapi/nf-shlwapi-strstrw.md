---
UID: NF:shlwapi.StrStrW
title: StrStrW function (shlwapi.h)
description: Finds the first occurrence of a substring within a string. The comparison is case-sensitive.helpviewer_keywords: ["StrStr","StrStr function [Windows Shell]","StrStrA","StrStrW","_win32_StrStr","shell.StrStr","shlwapi/StrStr","shlwapi/StrStrA","shlwapi/StrStrW"]
old-location: shell\StrStr.htm
tech.root: shell
ms.assetid: b1de5007-6773-4dea-8a15-ccd5f6924a13
ms.date: 12/05/2018
ms.keywords: StrStr, StrStr function [Windows Shell], StrStrA, StrStrW, _win32_StrStr, shell.StrStr, shlwapi/StrStr, shlwapi/StrStrA, shlwapi/StrStrW
f1_keywords:
- shlwapi/StrStr
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
req.unicode-ansi: StrStrW (Unicode) and StrStrA (ANSI)
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
- StrStr
- StrStrA
- StrStrW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrStrW function


## -description


Finds the first occurrence of a substring within a string. The comparison is case-sensitive.


## -parameters




### -param pszFirst [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string to search.


### -param pszSrch [in]

Type: <b>PCTSTR</b>

A pointer to the substring to search for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.



