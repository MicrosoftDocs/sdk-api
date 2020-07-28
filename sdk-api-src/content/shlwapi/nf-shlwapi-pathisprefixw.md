---
UID: NF:shlwapi.PathIsPrefixW
title: PathIsPrefixW function (shlwapi.h)
description: Searches a path to determine if it contains a valid prefix of the type passed by pszPrefix. A prefix is one of these types:\_&quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.
helpviewer_keywords: ["PathIsPrefix","PathIsPrefix function [Windows Shell]","PathIsPrefixA","PathIsPrefixW","_win32_PathIsPrefix","shell.PathIsPrefix","shlwapi/PathIsPrefix","shlwapi/PathIsPrefixA","shlwapi/PathIsPrefixW"]
old-location: shell\PathIsPrefix.htm
tech.root: shell
ms.assetid: b24f761e-6492-4a6d-9c7e-d5a5f2cbdaf3
ms.date: 12/05/2018
ms.keywords: PathIsPrefix, PathIsPrefix function [Windows Shell], PathIsPrefixA, PathIsPrefixW, _win32_PathIsPrefix, shell.PathIsPrefix, shlwapi/PathIsPrefix, shlwapi/PathIsPrefixA, shlwapi/PathIsPrefixW
f1_keywords:
- shlwapi/PathIsPrefix
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsPrefixW function


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



## -remarks

> [!NOTE]
> The shlwapi.h header defines PathIsPrefix as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

