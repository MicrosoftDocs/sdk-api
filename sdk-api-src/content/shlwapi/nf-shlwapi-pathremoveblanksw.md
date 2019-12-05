---
UID: NF:shlwapi.PathRemoveBlanksW
title: PathRemoveBlanksW function (shlwapi.h)
description: Removes all leading and trailing spaces from a string.
old-location: shell\PathRemoveBlanks.htm
tech.root: shell
ms.assetid: 0f496855-3ea7-4193-b895-fd4ea26ef6c5
ms.date: 12/05/2018
ms.keywords: PathRemoveBlanks, PathRemoveBlanks function [Windows Shell], PathRemoveBlanksA, PathRemoveBlanksW, _win32_PathRemoveBlanks, shell.PathRemoveBlanks, shlwapi/PathRemoveBlanks, shlwapi/PathRemoveBlanksA, shlwapi/PathRemoveBlanksW
ms.topic: function
f1_keywords:
- shlwapi/PathRemoveBlanks
dev_langs:
- c++
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
- PathRemoveBlanks
- PathRemoveBlanksA
- PathRemoveBlanksW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathRemoveBlanksW function


## -description


Removes all leading and trailing spaces from a string.


## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH from which to strip all leading and trailing spaces.


## -returns



This function does not return a value.



