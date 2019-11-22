---
UID: NF:shlwapi.PathIsUNCA
title: PathIsUNCA function (shlwapi.h)

description: Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.
old-location: shell\PathIsUNC.htm
tech.root: shell
ms.assetid: 53da5ba7-a2a4-45b2-90e0-ae006415933e

ms.date: 12/05/2018
ms.keywords: PathIsUNC, PathIsUNC function [Windows Shell], PathIsUNCA, PathIsUNCW, _win32_PathIsUNC, shell.PathIsUNC, shlwapi/PathIsUNC, shlwapi/PathIsUNCA, shlwapi/PathIsUNCW
ms.topic: function
f1_keywords: 
 - "shlwapi/PathIsUNC"
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
req.unicode-ansi: PathIsUNCW (Unicode) and PathIsUNCA (ANSI)
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
 - PathIsUNC
 - PathIsUNCA
 - PathIsUNCW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsUNCA function


## -description


Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to validate.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string is a valid UNC path; otherwise, <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/pathcch/nf-pathcch-pathisuncex">PathIsUNCEx</a>
 

 

