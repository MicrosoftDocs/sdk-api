---
UID: NF:shlwapi.PathIsDirectoryEmptyW
title: PathIsDirectoryEmptyW function (shlwapi.h)
author: windows-sdk-content
description: Determines whether a specified path is an empty directory.
old-location: shell\PathIsDirectoryEmpty.htm
tech.root: shell
ms.assetid: 833fe68e-8b21-4819-8370-d1b5391a3080
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PathIsDirectoryEmpty, PathIsDirectoryEmpty function [Windows Shell], PathIsDirectoryEmptyA, PathIsDirectoryEmptyW, _win32_PathIsDirectoryEmpty, shell.PathIsDirectoryEmpty, shlwapi/PathIsDirectoryEmpty, shlwapi/PathIsDirectoryEmptyA, shlwapi/PathIsDirectoryEmptyW
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsDirectoryEmptyW (Unicode) and PathIsDirectoryEmptyA (ANSI)
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
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - PathIsDirectoryEmpty
 - PathIsDirectoryEmptyA
 - PathIsDirectoryEmptyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathIsDirectoryEmptyW function


## -description


Determines whether a specified path is an empty directory.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be tested.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>pszPath</i> is an empty directory. Returns <b>FALSE</b> if <i>pszPath</i> is not a directory, or if it contains at least one file other than "." or "..".




## -remarks



"C:\" is considered a directory.




## -see-also




<a href="https://msdn.microsoft.com/9af3e3da-6b3a-4e81-ba50-ff7aeeb73c44">PathIsDirectory</a>
 

 

