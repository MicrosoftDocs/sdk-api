---
UID: NF:shlwapi.PathCommonPrefixA
title: PathCommonPrefixA function
author: windows-sdk-content
description: Compares two paths to determine if they share a common prefix. A prefix is one of these types:\_&#0034;C:\\&#0034;, &#0034;.&#0034;, &#0034;..&#0034;, &#0034;..\\&#0034;.
old-location: shell\PathCommonPrefix.htm
old-project: shell
ms.assetid: 13c32b32-8541-41c4-82d8-48d3b2439f0c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PathCommonPrefix, PathCommonPrefix function [Windows Shell], PathCommonPrefixA, PathCommonPrefixW, _win32_PathCommonPrefix, shell.PathCommonPrefix, shlwapi/PathCommonPrefix, shlwapi/PathCommonPrefixA, shlwapi/PathCommonPrefixW
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
req.unicode-ansi: PathCommonPrefixW (Unicode) and PathCommonPrefixA (ANSI)
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
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathCommonPrefix
 - PathCommonPrefixA
 - PathCommonPrefixW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathCommonPrefixA function


## -description


Compares two paths to determine if they share a common prefix. A prefix is one of these types: "C:\\", ".", "..", "..\\".


## -parameters




### -param pszFile1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the first path name.


### -param pszFile2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the second path name.


### -param achPath

TBD




#### - pszPath [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that receives the common prefix. This buffer must be at least MAX_PATH characters in size. If there is no common prefix, it is set to <b>NULL</b>.


## -returns



Type: <b>int</b>

Returns the count of common prefix characters in the path. If the output buffer pointer is not <b>NULL</b>, then these characters are copied to the output buffer.



