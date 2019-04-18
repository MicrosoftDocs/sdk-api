---
UID: NF:shlwapi.PathIsRelativeW
title: PathIsRelativeW function (shlwapi.h)
author: windows-sdk-content
description: Searches a path and determines if it is relative.
old-location: shell\PathIsRelative.htm
tech.root: shell
ms.assetid: ad36c277-645f-4c62-af7d-b75e29de573f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PathIsRelative, PathIsRelative function [Windows Shell], PathIsRelativeA, PathIsRelativeW, _win32_PathIsRelative, shell.PathIsRelative, shlwapi/PathIsRelative, shlwapi/PathIsRelativeA, shlwapi/PathIsRelativeW
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsRelativeW (Unicode) and PathIsRelativeA (ANSI)
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
 - PathIsRelative
 - PathIsRelativeA
 - PathIsRelativeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsRelativeW function


## -description


Searches a path and determines if it is relative.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path is relative, or <b>FALSE</b> if it is absolute.



