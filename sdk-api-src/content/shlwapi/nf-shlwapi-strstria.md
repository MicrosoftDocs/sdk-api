---
UID: NF:shlwapi.StrStrIA
title: StrStrIA function
author: windows-sdk-content
description: Finds the first occurrence of a substring within a string. The comparison is not case-sensitive.
old-location: shell\StrStrI.htm
old-project: shell
ms.assetid: b0281641-1375-4815-a707-03e1ce7e5a29
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: StrStrI, StrStrI function [Windows Shell], StrStrIA, StrStrIW, _win32_StrStrI, shell.StrStrI, shlwapi/StrStrI, shlwapi/StrStrIA, shlwapi/StrStrIW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrStrIW (Unicode) and StrStrIA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
 - StrStrI
 - StrStrIA
 - StrStrIW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# StrStrIA function


## -description


Finds the first occurrence of a substring within a string. The comparison is not case-sensitive.


## -parameters




### -param pszFirst [in]

Type: <b>PTSTR</b>

A pointer to the null-terminated string being searched.


### -param pszSrch [in]

Type: <b>PCTSTR</b>

A pointer to the substring to search for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the first occurrence of the matching substring if successful, or <b>NULL</b> otherwise.



