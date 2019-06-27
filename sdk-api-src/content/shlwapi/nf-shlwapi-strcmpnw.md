---
UID: NF:shlwapi.StrCmpNW
title: StrCmpNW function (shlwapi.h)
author: windows-sdk-content
description: Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is case-sensitive. The StrNCmp macro differs from this function in name only.
old-location: shell\StrCmpN.htm
tech.root: shell
ms.assetid: e2d97502-1819-463e-a56a-2d22b33502b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StrCmpN, StrCmpN function [Windows Shell], StrCmpNA, StrCmpNW, _win32_StrCmpN, shell.StrCmpN, shlwapi/StrCmpN, shlwapi/StrCmpNA, shlwapi/StrCmpNW
ms.topic: function
f1_keywords: 
 - "shlwapi/StrCmpN"
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpNW (Unicode) and StrCmpNA (ANSI)
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
 - StrCmpN
 - StrCmpNA
 - StrCmpNW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrCmpNW function


## -description


Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is case-sensitive. The <b>StrNCmp</b> macro differs from this function in name only.


## -parameters




### -param psz1 [in]

Type: <b>PCTSTR</b>

A pointer to the first null-terminated string to be compared.


### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to the second null-terminated string to be compared.


### -param nChar [in]

Type: <b>int</b>

The number of characters from the beginning of each string to be compared.


## -returns



Type: <b>int</b>

Returns zero if the strings are identical. Returns a positive value if the first <i>nChar</i> characters of the string pointed to by <i>psz1</i> are greater than those from the string pointed to by <i>psz2</i>. It returns a negative value if the first <i>nChar</i> characters of the string pointed to by <i>psz1</i> are less than those from the string pointed to by <i>psz2</i>.



