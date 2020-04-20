---
UID: NF:shlwapi.PathSkipRootA
title: PathSkipRootA function (shlwapi.h)
description: Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.helpviewer_keywords: ["PathSkipRoot","PathSkipRoot function [Windows Shell]","PathSkipRootA","PathSkipRootW","_win32_PathSkipRoot","shell.PathSkipRoot","shlwapi/PathSkipRoot","shlwapi/PathSkipRootA","shlwapi/PathSkipRootW"]
old-location: shell\PathSkipRoot.htm
tech.root: shell
ms.assetid: 528a3953-26d7-4fff-be31-9c9788d429ab
ms.date: 12/05/2018
ms.keywords: PathSkipRoot, PathSkipRoot function [Windows Shell], PathSkipRootA, PathSkipRootW, _win32_PathSkipRoot, shell.PathSkipRoot, shlwapi/PathSkipRoot, shlwapi/PathSkipRootA, shlwapi/PathSkipRootW
f1_keywords:
- shlwapi/PathSkipRoot
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
req.unicode-ansi: PathSkipRootW (Unicode) and PathSkipRootA (ANSI)
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
- PathSkipRoot
- PathSkipRootA
- PathSkipRootW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathSkipRootA function


## -description


Retrieves a pointer to the first character in a path following the drive letter or Universal Naming Convention (UNC) server/share path elements.


## -parameters




### -param pszPath [in]

Type: <b>PTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to parse.


## -returns



Type: <b>PTSTR</b>

A pointer that, when this function returns successfully, points to the beginning of the subpath that follows the root (drive letter or UNC server/share). If the function encounters an error, this value will be <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pathcch/nf-pathcch-pathcchskiproot">PathCchSkipRoot</a>
 

 

