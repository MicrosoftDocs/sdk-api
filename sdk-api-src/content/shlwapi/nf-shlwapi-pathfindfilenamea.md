---
UID: NF:shlwapi.PathFindFileNameA
title: PathFindFileNameA function (shlwapi.h)
description: Searches a path for a file name.helpviewer_keywords: ["PathFindFileName","PathFindFileName function [Windows Shell]","PathFindFileNameA","PathFindFileNameW","_win32_PathFindFileName","shell.PathFindFileName","shlwapi/PathFindFileName","shlwapi/PathFindFileNameA","shlwapi/PathFindFileNameW"]
old-location: shell\PathFindFileName.htm
tech.root: shell
ms.assetid: f3824dee-1169-4f89-9844-35aa8a1830c4
ms.date: 12/05/2018
ms.keywords: PathFindFileName, PathFindFileName function [Windows Shell], PathFindFileNameA, PathFindFileNameW, _win32_PathFindFileName, shell.PathFindFileName, shlwapi/PathFindFileName, shlwapi/PathFindFileNameA, shlwapi/PathFindFileNameW
f1_keywords:
- shlwapi/PathFindFileName
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
req.unicode-ansi: PathFindFileNameW (Unicode) and PathFindFileNameA (ANSI)
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
- PathFindFileName
- PathFindFileNameA
- PathFindFileNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathFindFileNameA function


## -description


Searches a path for a file name.


## -parameters




### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search.


## -returns



Type: <b>PTSTR</b>

Returns a pointer to the address of the string if successful, or a pointer to the beginning of the path otherwise.



