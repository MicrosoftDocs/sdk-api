---
UID: NF:shlwapi.StrChrNW
title: StrChrNW function (shlwapi.h)
description: Searches a string for the first occurrence of a specified character. The comparison is case-sensitive.
helpviewer_keywords: ["StrChrNW","StrChrNW function [Windows Shell]","_win32_StrChrNW","shell.StrChrNW","shlwapi/StrChrNW"]
old-location: shell\StrChrNW.htm
tech.root: shell
ms.assetid: f90470c3-62db-4fbb-a045-8fdd300a6aa4
ms.date: 12/05/2018
ms.keywords: StrChrNW, StrChrNW function [Windows Shell], _win32_StrChrNW, shell.StrChrNW, shlwapi/StrChrNW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrChrNW
 - shlwapi/StrChrNW
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
 - StrChrNW
---

# StrChrNW function


## -description

Searches a string for the first occurrence of a specified character. The comparison is case-sensitive.

## -parameters

### -param pszStart [in]

Type: <b>PWSTR</b>

A pointer to the string to be searched.

### -param wMatch

Type: <b>WCHAR</b>

The character to be used for comparison.

### -param cchMax

Type: <b>UINT</b>

The maximum number of characters to search.

## -returns

Type: <b>PWSTR</b>

Returns the address of the first occurrence of the character in the string if successful, or <b>NULL</b> otherwise.

## -remarks

<b>StrChrNW</b> searches for <i>wMatch</i> from <i>pszStart</i> to <i>pszStart</i> + <i>cchMax</i>, or until a <b>NULL</b> character is encountered.

To help ensure optimal performance, <i>pszStart</i> should be word-aligned.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strchra">StrChr</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strchria">StrChrI</a>