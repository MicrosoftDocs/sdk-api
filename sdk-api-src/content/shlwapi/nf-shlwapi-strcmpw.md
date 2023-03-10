---
UID: NF:shlwapi.StrCmpW
title: StrCmpW function (shlwapi.h)
description: Compares two strings to determine if they are the same. The comparison is case-sensitive.
helpviewer_keywords: ["StrCmp","StrCmp function [Windows Shell]","StrCmpW","_win32_StrCmp","shell.StrCmp","shlwapi/StrCmp","shlwapi/StrCmpW"]
old-location: shell\StrCmp.htm
tech.root: shell
ms.assetid: 12530a04-776c-4506-86d1-07e2c3569a36
ms.date: 12/05/2018
ms.keywords: StrCmp, StrCmp function [Windows Shell], StrCmpW, _win32_StrCmp, shell.StrCmp, shlwapi/StrCmp, shlwapi/StrCmpW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrCmpW
 - shlwapi/StrCmpW
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
 - StrCmp
 - StrCmpW
---

# StrCmpW function


## -description

Compares two strings to determine if they are the same. The comparison is case-sensitive.

## -parameters

### -param psz1 [in]

Type: <b>PCTSTR</b>

A pointer to the first null-terminated string to be compared.

### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to the second null-terminated string to be compared.

## -returns

Type: <b>int</b>

Returns zero if the strings are identical. Returns a positive value if the string pointed to by <i>psz1</i> is greater than that pointed to by <i>psz2</i>. Returns a negative value if the string pointed to by <i>psz1</i> is less than that pointed to by <i>psz2</i>.

