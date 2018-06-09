---
UID: NF:shlwapi.StrCmpNIA
title: StrCmpNIA function
author: windows-sdk-content
description: Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is not case-sensitive. The StrNCmpI macro differs from this function in name only.
old-location: shell\StrCmpNI.htm
old-project: shell
ms.assetid: c6657bd5-21b6-457c-9ed0-45e44b2571ba
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: StrCmpNI, StrCmpNI function [Windows Shell], StrCmpNIA, StrCmpNIW, _win32_StrCmpNI, shell.StrCmpNI, shlwapi/StrCmpNI, shlwapi/StrCmpNIA, shlwapi/StrCmpNIW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCmpNIW (Unicode) and StrCmpNIA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
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
 - StrCmpNI
 - StrCmpNIA
 - StrCmpNIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrCmpNIA function


## -description


Compares a specified number of characters from the beginning of two strings to determine if they are the same. The comparison is not case-sensitive. The <b>StrNCmpI</b> macro differs from this function in name only.


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



