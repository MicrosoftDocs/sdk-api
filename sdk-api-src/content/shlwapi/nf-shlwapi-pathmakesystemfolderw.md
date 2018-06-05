---
UID: NF:shlwapi.PathMakeSystemFolderW
title: PathMakeSystemFolderW function
author: windows-sdk-content
description: Gives an existing folder the proper attributes to become a system folder.
old-location: shell\PathMakeSystemFolder.htm
old-project: shell
ms.assetid: 5b0faeb8-f8ae-481b-b5b2-cae9efe638e5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PathMakeSystemFolder, PathMakeSystemFolder function [Windows Shell], PathMakeSystemFolderA, PathMakeSystemFolderW, _win32_PathMakeSystemFolder, shell.PathMakeSystemFolder, shlwapi/PathMakeSystemFolder, shlwapi/PathMakeSystemFolderA, shlwapi/PathMakeSystemFolderW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathMakeSystemFolderW (Unicode) and PathMakeSystemFolderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
-	api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
-	PathMakeSystemFolder
-	PathMakeSystemFolderA
-	PathMakeSystemFolderW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathMakeSystemFolderW function


## -description


Gives an existing folder the proper attributes to become a system folder.


## -parameters




### -param pszPath [in]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the name of an existing folder that will be made into a system folder.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.



