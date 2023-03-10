---
UID: NF:shlwapi.StrStrNW
title: StrStrNW function (shlwapi.h)
description: Finds the first occurrence of a substring within a string. The comparison is case-sensitive. (StrStrNW)
helpviewer_keywords: ["StrStrNW","StrStrNW function [Windows Shell]","_shell_StrStrNW","shell.StrStrNW","shlwapi/StrStrNW"]
old-location: shell\StrStrNW.htm
tech.root: shell
ms.assetid: e7aac4c7-b2d5-43d8-97f5-1b11ebb24ee1
ms.date: 12/05/2018
ms.keywords: StrStrNW, StrStrNW function [Windows Shell], _shell_StrStrNW, shell.StrStrNW, shlwapi/StrStrNW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrStrNW
 - shlwapi/StrStrNW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrStrNW
---

# StrStrNW function


## -description

Finds the first occurrence of a substring within a string. The comparison is case-sensitive.

## -parameters

### -param pszFirst [in]

Type: <b>PWSTR</b>

A pointer to the null-terminated, Unicode string that is being searched.

### -param pszSrch [in]

Type: <b>PCWSTR</b>

A pointer to the null-terminated, Unicode substring that is being searched for.

### -param cchMax

Type: <b>UINT</b>

The maximum number of characters from the beginning of the searched string in which to search for the substring.

## -returns

Type: <b>PWSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.

