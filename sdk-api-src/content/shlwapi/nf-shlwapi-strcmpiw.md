---
UID: NF:shlwapi.StrCmpIW
title: StrCmpIW function
author: windows-sdk-content
description: Compares two strings to determine if they are the same. The comparison is not case-sensitive.
old-location: shell\StrCmpI.htm
old-project: shell
ms.assetid: d059b6bd-8f03-4273-aa7a-b8b07f84d268
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: StrCmpI, StrCmpI function [Windows Shell], StrCmpIW, _win32_StrCmpI, shell.StrCmpI, shlwapi/StrCmpI, shlwapi/StrCmpIW
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
req.unicode-ansi: StrCmpIW (Unicode)
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
 - StrCmpI
 - StrCmpIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrCmpIW function


## -description


Compares two strings to determine if they are the same. The comparison is not case-sensitive.


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



