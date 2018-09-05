---
UID: NF:shlwapi.PathMatchSpecA
title: PathMatchSpecA function
author: windows-sdk-content
description: Searches a string using a Microsoft MS-DOS wildcard match type.
old-location: shell\PathMatchSpec.htm
old-project: shell
ms.assetid: 908e7204-d168-4179-9c7b-ad46ba68bebc
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: PathMatchSpec, PathMatchSpec function [Windows Shell], PathMatchSpecA, PathMatchSpecW, _win32_PathMatchSpec, shell.PathMatchSpec, shlwapi/PathMatchSpec, shlwapi/PathMatchSpecA, shlwapi/PathMatchSpecW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathMatchSpecW (Unicode) and PathMatchSpecA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathMatchSpec
 - PathMatchSpecA
 - PathMatchSpecW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathMatchSpecA function


## -description


Searches a string using a Microsoft MS-DOS wildcard match type.


## -parameters




### -param pszFile [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.


### -param pszSpec [in]

Type: <b>LPCSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file type for which to search. For example, to test whether <i>pszFile</i> is a .doc file, <i>pszSpec</i> should be set to "*.doc".


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string matches, or <b>FALSE</b> otherwise.



