---
UID: NF:shlwapi.PathIsDirectoryA
title: PathIsDirectoryA function
author: windows-sdk-content
description: Verifies that a path is a valid directory.
old-location: shell\PathIsDirectory.htm
tech.root: shell
ms.assetid: 9af3e3da-6b3a-4e81-ba50-ff7aeeb73c44
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: PathIsDirectory, PathIsDirectory function [Windows Shell], PathIsDirectoryA, PathIsDirectoryW, _win32_PathIsDirectory, shell.PathIsDirectory, shlwapi/PathIsDirectory, shlwapi/PathIsDirectoryA, shlwapi/PathIsDirectoryW
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
req.unicode-ansi: PathIsDirectoryW (Unicode) and PathIsDirectoryA (ANSI)
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
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
 - Ext-MS-Win-shell-shlwapi-l1-1-0.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - PathIsDirectory
 - PathIsDirectoryA
 - PathIsDirectoryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathIsDirectoryA function


## -description


Verifies that a path is a valid directory.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to verify.


## -returns



Type: <b>BOOL</b>

Returns (BOOL)FILE_ATTRIBUTE_DIRECTORY if the path is a valid directory; otherwise, <b>FALSE</b>.



