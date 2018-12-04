---
UID: NF:shlwapi.PathIsPrefixA
title: PathIsPrefixA function
author: windows-sdk-content
description: Searches a path to determine if it contains a valid prefix of the type passed by pszPrefix. A prefix is one of these types:\_&#0034;C:\\&#0034;, &#0034;.&#0034;, &#0034;..&#0034;, &#0034;..\\&#0034;.
old-location: shell\PathIsPrefix.htm
tech.root: shell
ms.assetid: b24f761e-6492-4a6d-9c7e-d5a5f2cbdaf3
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: PathIsPrefix, PathIsPrefix function [Windows Shell], PathIsPrefixA, PathIsPrefixW, _win32_PathIsPrefix, shell.PathIsPrefix, shlwapi/PathIsPrefix, shlwapi/PathIsPrefixA, shlwapi/PathIsPrefixW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsPrefixW (Unicode) and PathIsPrefixA (ANSI)
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
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathIsPrefix
 - PathIsPrefixA
 - PathIsPrefixW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathIsPrefixA function


## -description


Searches a path to determine if it contains a valid prefix of the type passed by <i>pszPrefix</i>. A prefix is one of these types: "C:\\", ".", "..", "..\\".


## -parameters




### -param pszPrefix [in]

Type: <b>IN LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the prefix for which to search.


### -param pszPath [in]

Type: <b>IN LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the compared path is the full prefix for the path, or <b>FALSE</b> otherwise.



