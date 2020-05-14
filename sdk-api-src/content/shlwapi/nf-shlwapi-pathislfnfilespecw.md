---
UID: NF:shlwapi.PathIsLFNFileSpecW
title: PathIsLFNFileSpecW function (shlwapi.h)
description: Determines whether a file name is in long format.helpviewer_keywords: ["PathIsLFNFileSpec","PathIsLFNFileSpec function [Windows Shell]","PathIsLFNFileSpecA","PathIsLFNFileSpecW","_win32_PathIsLFNFileSpec","shell.PathIsLFNFileSpec","shlwapi/PathIsLFNFileSpec","shlwapi/PathIsLFNFileSpecA","shlwapi/PathIsLFNFileSpecW"]
old-location: shell\PathIsLFNFileSpec.htm
tech.root: shell
ms.assetid: 599cb457-da72-4416-bfb7-5bc55a0eeb2d
ms.date: 12/05/2018
ms.keywords: PathIsLFNFileSpec, PathIsLFNFileSpec function [Windows Shell], PathIsLFNFileSpecA, PathIsLFNFileSpecW, _win32_PathIsLFNFileSpec, shell.PathIsLFNFileSpec, shlwapi/PathIsLFNFileSpec, shlwapi/PathIsLFNFileSpecA, shlwapi/PathIsLFNFileSpecW
f1_keywords:
- shlwapi/PathIsLFNFileSpec
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
req.unicode-ansi: PathIsLFNFileSpecW (Unicode) and PathIsLFNFileSpecA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
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
- PathIsLFNFileSpec
- PathIsLFNFileSpecA
- PathIsLFNFileSpecW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsLFNFileSpecW function


## -description


Determines whether a file name is in long format.


## -parameters




### -param pszName [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file name to be tested.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszName</i> exceeds the number of characters allowed by the 8.3 format, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-pathisfilespeca">PathIsFileSpec</a>
 

 

