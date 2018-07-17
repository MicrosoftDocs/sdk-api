---
UID: NF:shlwapi.PathRemoveBlanksA
title: PathRemoveBlanksA function
author: windows-sdk-content
description: Removes all leading and trailing spaces from a string.
old-location: shell\PathRemoveBlanks.htm
old-project: shell
ms.assetid: 0f496855-3ea7-4193-b895-fd4ea26ef6c5
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PathRemoveBlanks, PathRemoveBlanks function [Windows Shell], PathRemoveBlanksA, PathRemoveBlanksW, _win32_PathRemoveBlanks, shell.PathRemoveBlanks, shlwapi/PathRemoveBlanks, shlwapi/PathRemoveBlanksA, shlwapi/PathRemoveBlanksW
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
req.unicode-ansi: PathRemoveBlanksW (Unicode) and PathRemoveBlanksA (ANSI)
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
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathRemoveBlanks
 - PathRemoveBlanksA
 - PathRemoveBlanksW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathRemoveBlanksA function


## -description


Removes all leading and trailing spaces from a string.


## -parameters




### -param pszPath

TBD




#### - lpszString [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH from which to strip all leading and trailing spaces.


## -returns



This function does not return a value.



