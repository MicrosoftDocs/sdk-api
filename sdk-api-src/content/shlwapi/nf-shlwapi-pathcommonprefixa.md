---
UID: NF:shlwapi.PathCommonPrefixA
title: PathCommonPrefixA function (shlwapi.h)
description: Compares two paths to determine if they share a common prefix. A prefix is one of these types:\_&quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;. (ANSI)
helpviewer_keywords: ["PathCommonPrefixA", "shlwapi/PathCommonPrefixA"]
old-location: shell\PathCommonPrefix.htm
tech.root: shell
ms.assetid: 13c32b32-8541-41c4-82d8-48d3b2439f0c
ms.date: 12/05/2018
ms.keywords: PathCommonPrefix, PathCommonPrefix function [Windows Shell], PathCommonPrefixA, PathCommonPrefixW, _win32_PathCommonPrefix, shell.PathCommonPrefix, shlwapi/PathCommonPrefix, shlwapi/PathCommonPrefixA, shlwapi/PathCommonPrefixW
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathCommonPrefixA
 - shlwapi/PathCommonPrefixA
dev_langs:
 - c++
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

### -param achPath [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that receives the common prefix. This buffer must be at least MAX_PATH characters in size. If there is no common prefix, it is set to <b>NULL</b>.

## -returns

Type: <b>int</b>

Returns the count of common prefix characters in the path. If the output buffer pointer is not <b>NULL</b>, then these characters are copied to the output buffer.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathCommonPrefix as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

