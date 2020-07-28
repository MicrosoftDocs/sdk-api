---
UID: NF:shlwapi.PathIsUNCServerW
title: PathIsUNCServerW function (shlwapi.h)
description: Determines if a string is a valid Universal Naming Convention (UNC) for a server path only.
helpviewer_keywords: ["PathIsUNCServer","PathIsUNCServer function [Windows Shell]","PathIsUNCServerA","PathIsUNCServerW","_win32_PathIsUNCServer","shell.PathIsUNCServer","shlwapi/PathIsUNCServer","shlwapi/PathIsUNCServerA","shlwapi/PathIsUNCServerW"]
old-location: shell\PathIsUNCServer.htm
tech.root: shell
ms.assetid: 9158ceb6-dd20-4b1a-93d3-cf7a5a5c6c75
ms.date: 12/05/2018
ms.keywords: PathIsUNCServer, PathIsUNCServer function [Windows Shell], PathIsUNCServerA, PathIsUNCServerW, _win32_PathIsUNCServer, shell.PathIsUNCServer, shlwapi/PathIsUNCServer, shlwapi/PathIsUNCServerA, shlwapi/PathIsUNCServerW
f1_keywords:
- shlwapi/PathIsUNCServer
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
req.unicode-ansi: PathIsUNCServerW (Unicode) and PathIsUNCServerA (ANSI)
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
- PathIsUNCServer
- PathIsUNCServerA
- PathIsUNCServerW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsUNCServerW function


## -description


Determines if a string is a valid Universal Naming Convention (UNC) for a server path only.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to validate.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string is a valid UNC path for a server only (no share name), or <b>FALSE</b> otherwise.



## -remarks

> [!NOTE]
> The shlwapi.h header defines PathIsUNCServer as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

