---
UID: NF:shlwapi.PathFindOnPathW
title: PathFindOnPathW function (shlwapi.h)
description: Searches for a file. (Unicode)
helpviewer_keywords: ["PathFindOnPath", "PathFindOnPath function [Windows Shell]", "PathFindOnPathW", "_win32_PathFindOnPath", "shell.PathFindOnPath", "shlwapi/PathFindOnPath", "shlwapi/PathFindOnPathW"]
old-location: shell\PathFindOnPath.htm
tech.root: shell
ms.assetid: d9281eb2-39b7-444f-85b7-1e1e76c38ae2
ms.date: 12/05/2018
ms.keywords: PathFindOnPath, PathFindOnPath function [Windows Shell], PathFindOnPathA, PathFindOnPathW, _win32_PathFindOnPath, shell.PathFindOnPath, shlwapi/PathFindOnPath, shlwapi/PathFindOnPathA, shlwapi/PathFindOnPathW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathFindOnPathW (Unicode) and PathFindOnPathA (ANSI)
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
 - PathFindOnPathW
 - shlwapi/PathFindOnPathW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathFindOnPath
 - PathFindOnPathA
 - PathFindOnPathW
---

# PathFindOnPathW function


## -description

Searches for a file.

## -parameters

### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the file name for which to search. If the search is successful, this parameter is used to return the fully qualified path name.

### -param ppszOtherDirs [in, optional]

Type: <b>LPCTSTR*</b>

An optional, null-terminated array of directories to be searched first. This value can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

<b>PathFindOnPath</b> searches for the file specified by <i>pszFile</i>. If no directories are specified in <i>ppszOtherDirs</i>, it attempts to find the file by searching standard directories such as System32 and the directories specified in the PATH environment variable. To expedite the process or enable <b>PathFindOnPath</b> to search a wider range of directories, use the <i>ppszOtherDirs</i> parameter to specify one or more directories to be searched first. If more than one file has the name specified by <i>pszFile</i>, <b>PathFindOnPath</b> returns the first instance it finds.




> [!NOTE]
> The shlwapi.h header defines PathFindOnPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

