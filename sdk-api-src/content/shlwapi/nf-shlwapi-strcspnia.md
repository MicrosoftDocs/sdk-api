---
UID: NF:shlwapi.StrCSpnIA
title: StrCSpnIA function (shlwapi.h)
description: Searches a string for the first occurrence of any of a group of characters. The search method is not case-sensitive, and the terminating NULL character is included within the search pattern match. (ANSI)
helpviewer_keywords: ["StrCSpnIA", "shlwapi/StrCSpnIA"]
old-location: shell\StrCSpnI.htm
tech.root: shell
ms.assetid: d21eb80b-5f02-4eb7-9a22-02425b7050b3
ms.date: 12/05/2018
ms.keywords: StrCSpnI, StrCSpnI function [Windows Shell], StrCSpnIA, StrCSpnIW, _win32_StrCSpnI, shell.StrCSpnI, shlwapi/StrCSpnI, shlwapi/StrCSpnIA, shlwapi/StrCSpnIW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCSpnIW (Unicode) and StrCSpnIA (ANSI)
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
 - StrCSpnIA
 - shlwapi/StrCSpnIA
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
 - StrCSpnI
 - StrCSpnIA
 - StrCSpnIW
---

# StrCSpnIA function


## -description

Searches a string for the first occurrence of any of a group of characters. The search method is not case-sensitive, and the terminating <b>NULL</b> character is included within the search pattern match.

## -parameters

### -param pszStr [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated string to be searched.

### -param pszSet [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string containing the characters to search for.

## -returns

Type: <b>int</b>

Returns the index of the first occurrence in <i>pszStr</i> of any character from <i>pszSet</i>, or the length of <i>pszStr</i> if no match is found.

## -remarks

The return value of this function is equal to the length of the initial substring in <i>pszStr</i> that does not include any characters from <i>pszSet</i>.




> [!NOTE]
> The shlwapi.h header defines StrCSpnI as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

