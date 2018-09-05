---
UID: NF:shlwapi.PathIsSameRootW
title: PathIsSameRootW function
author: windows-sdk-content
description: Compares two paths to determine if they have a common root component.
old-location: shell\PathIsSameRoot.htm
old-project: shell
ms.assetid: 3409a8f1-e22c-4c13-961e-211a2d10fe10
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: PathIsSameRoot, PathIsSameRoot function [Windows Shell], PathIsSameRootA, PathIsSameRootW, _win32_PathIsSameRoot, shell.PathIsSameRoot, shlwapi/PathIsSameRoot, shlwapi/PathIsSameRootA, shlwapi/PathIsSameRootW
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
req.unicode-ansi: PathIsSameRootW (Unicode) and PathIsSameRootA (ANSI)
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
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathIsSameRoot
 - PathIsSameRootA
 - PathIsSameRootW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathIsSameRootW function


## -description


Compares two paths to determine if they have a common root component.


## -parameters




### -param pszPath1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the first path to be compared.


### -param pszPath2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the second path to be compared.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if both strings have the same root component, or <b>FALSE</b> otherwise. If <i>pszPath1</i> contains only the server and share, this function also returns <b>FALSE</b>.



