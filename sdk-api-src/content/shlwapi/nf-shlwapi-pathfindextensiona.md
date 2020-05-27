---
UID: NF:shlwapi.PathFindExtensionA
title: PathFindExtensionA function (shlwapi.h)
description: Searches a path for an extension.
helpviewer_keywords: ["PathFindExtension","PathFindExtension function [Windows Shell]","PathFindExtensionA","PathFindExtensionW","_win32_PathFindExtension","shell.PathFindExtension","shlwapi/PathFindExtension","shlwapi/PathFindExtensionA","shlwapi/PathFindExtensionW"]
old-location: shell\PathFindExtension.htm
tech.root: shell
ms.assetid: afebd4b7-2685-4b6e-8f8a-d43944dacef5
ms.date: 12/05/2018
ms.keywords: PathFindExtension, PathFindExtension function [Windows Shell], PathFindExtensionA, PathFindExtensionW, _win32_PathFindExtension, shell.PathFindExtension, shlwapi/PathFindExtension, shlwapi/PathFindExtensionA, shlwapi/PathFindExtensionW
f1_keywords:
- shlwapi/PathFindExtension
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
req.unicode-ansi: PathFindExtensionW (Unicode) and PathFindExtensionA (ANSI)
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
- PathFindExtension
- PathFindExtensionA
- PathFindExtensionW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathFindExtensionA function


## -description


Searches a path for an extension.


## -parameters




### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search, including the extension being searched for.


## -returns



Type: <b>PTSTR</b>

Returns the address of the "." that precedes the extension within <i>pszPath</i> if an extension is found, or the address of the terminating null character otherwise.




## -remarks



Note that a valid file name extension cannot contain a space. For more information on valid file name extensions, see <a href="https://docs.microsoft.com/windows/desktop/shell/fa-file-extensions">File Type Handlers</a>.



