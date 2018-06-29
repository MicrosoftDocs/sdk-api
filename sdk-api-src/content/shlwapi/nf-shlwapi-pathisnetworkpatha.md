---
UID: NF:shlwapi.PathIsNetworkPathA
title: PathIsNetworkPathA function
author: windows-sdk-content
description: Determines whether a path string represents a network resource.
old-location: shell\PathIsNetworkPath.htm
old-project: shell
ms.assetid: 3a9c33bc-2325-4285-b6c3-4c3e1d323c1e
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: PathIsNetworkPath, PathIsNetworkPath function [Windows Shell], PathIsNetworkPathA, PathIsNetworkPathW, _win32_PathIsNetworkPath, shell.PathIsNetworkPath, shlwapi/PathIsNetworkPath, shlwapi/PathIsNetworkPathA, shlwapi/PathIsNetworkPathW
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
req.unicode-ansi: PathIsNetworkPathW (Unicode) and PathIsNetworkPathA (ANSI)
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
 - Ext-MS-Win-shell-shlwapi-l1-1-0.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - PathIsNetworkPath
 - PathIsNetworkPathA
 - PathIsNetworkPathW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathIsNetworkPathA function


## -description


Determines whether a path string represents a network resource.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string represents a network resource, or <b>FALSE</b> otherwise.




## -remarks



<b>PathIsNetworkPath</b> interprets the following two types of paths as network paths.

<ul>
<li>Paths that begin with two backslash characters (\\) are interpreted as Universal Naming Convention (UNC) paths.</li>
<li>Paths that begin with a letter followed by a colon (:) are interpreted as a mounted network drive. However, <b>PathIsNetworkPath</b> cannot recognize a network drive mapped to a drive letter through the Microsoft MS-DOS SUBST command or the <a href="https://msdn.microsoft.com/924b1456-b2c5-4d52-aacf-6172608c73ea">DefineDosDevice</a> function.</li>
</ul>
<div class="alert"><b>Note</b>  The function does not verify that the specified network resource exists, is currently accessible, or that the user has sufficient permissions to access it.</div>
<div> </div>


