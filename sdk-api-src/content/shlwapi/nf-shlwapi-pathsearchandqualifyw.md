---
UID: NF:shlwapi.PathSearchAndQualifyW
title: PathSearchAndQualifyW function
author: windows-sdk-content
description: Determines if a given path is correctly formatted and fully qualified.
old-location: shell\PathSearchAndQualify.htm
old-project: shell
ms.assetid: 90da281d-349a-460a-aa5a-14e3b4ced727
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PathSearchAndQualify, PathSearchAndQualify function [Windows Shell], PathSearchAndQualifyA, PathSearchAndQualifyW, _win32_PathSearchAndQualify, shell.PathSearchAndQualify, shlwapi/PathSearchAndQualify, shlwapi/PathSearchAndQualifyA, shlwapi/PathSearchAndQualifyW
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
req.unicode-ansi: PathSearchAndQualifyW (Unicode) and PathSearchAndQualifyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
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
 - PathSearchAndQualify
 - PathSearchAndQualifyA
 - PathSearchAndQualifyW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathSearchAndQualifyW function


## -description


Determines if a given path is correctly formatted and fully qualified.


## -parameters




### -param pszPath

TBD


### -param pszBuf

TBD


### -param cchBuf

TBD




#### - cchFullyQualifiedPath [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszFullyQualifiedPath</i>, in characters.


#### - pcszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to search.


#### - pszFullyQualifiedPath [out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path to be referenced.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the path is qualified, or <b>FALSE</b> otherwise.



