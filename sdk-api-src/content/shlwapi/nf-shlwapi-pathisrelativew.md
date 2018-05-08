---
UID: NF:shlwapi.PathIsRelativeW
title: PathIsRelativeW function
author: windows-driver-content
description: Searches a path and determines if it is relative.
old-location: shell\PathIsRelative.htm
old-project: shell
ms.assetid: ad36c277-645f-4c62-af7d-b75e29de573f
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: PathIsRelative, PathIsRelative function [Windows Shell], PathIsRelativeA, PathIsRelativeW, _win32_PathIsRelative, shell.PathIsRelative, shlwapi/PathIsRelative, shlwapi/PathIsRelativeA, shlwapi/PathIsRelativeW
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
-	PathIsRelative
-	PathIsRelativeA
-	PathIsRelativeW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathIsRelativeW function


## -description


Searches a path and determines if it is relative.


## -parameters




### -param pszPath

TBD




#### - lpszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path is relative, or <b>FALSE</b> if it is absolute.



