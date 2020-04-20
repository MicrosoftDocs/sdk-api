---
UID: NF:shlwapi.PathUnquoteSpacesW
title: PathUnquoteSpacesW function (shlwapi.h)
description: Removes quotes from the beginning and end of a path.helpviewer_keywords: ["PathUnquoteSpaces","PathUnquoteSpaces function [Windows Shell]","PathUnquoteSpacesA","PathUnquoteSpacesW","_win32_PathUnquoteSpaces","shell.PathUnquoteSpaces","shlwapi/PathUnquoteSpaces","shlwapi/PathUnquoteSpacesA","shlwapi/PathUnquoteSpacesW"]
old-location: shell\PathUnquoteSpaces.htm
tech.root: shell
ms.assetid: 00474c95-ec59-489a-bee3-191b98a47567
ms.date: 12/05/2018
ms.keywords: PathUnquoteSpaces, PathUnquoteSpaces function [Windows Shell], PathUnquoteSpacesA, PathUnquoteSpacesW, _win32_PathUnquoteSpaces, shell.PathUnquoteSpaces, shlwapi/PathUnquoteSpaces, shlwapi/PathUnquoteSpacesA, shlwapi/PathUnquoteSpacesW
f1_keywords:
- shlwapi/PathUnquoteSpaces
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
req.unicode-ansi: PathUnquoteSpacesW (Unicode) and PathUnquoteSpacesA (ANSI)
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
- PathUnquoteSpaces
- PathUnquoteSpacesA
- PathUnquoteSpacesW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathUnquoteSpacesW function


## -description


Removes quotes from the beginning and end of a path.


## -parameters




### -param lpsz [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path. When the function returns successfully, points to the string with beginning and ending quotation marks removed.


## -returns



No return value.



