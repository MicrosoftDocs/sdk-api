---
UID: NF:shlwapi.PathIsFileSpecA
title: PathIsFileSpecA function
author: windows-sdk-content
description: Searches a path for any path-delimiting characters (for example, ':' or '\' ). If there are no path-delimiting characters present, the path is considered to be a File Spec path.
old-location: shell\PathIsFileSpec.htm
tech.root: shell
ms.assetid: c69d6cca-44e7-4792-8fb2-3c4ecd2e57f2
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: PathIsFileSpec, PathIsFileSpec function [Windows Shell], PathIsFileSpecA, PathIsFileSpecW, _win32_PathIsFileSpec, shell.PathIsFileSpec, shlwapi/PathIsFileSpec, shlwapi/PathIsFileSpecA, shlwapi/PathIsFileSpecW
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
req.unicode-ansi: PathIsFileSpecW (Unicode) and PathIsFileSpecA (ANSI)
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
 - PathIsFileSpec
 - PathIsFileSpecA
 - PathIsFileSpecW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathIsFileSpecA function


## -description


Searches a path for any path-delimiting characters (for example, ':' or '\' ). If there are no path-delimiting characters present, the path is considered to be a File Spec path.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if there are no path-delimiting characters within the path, or <b>FALSE</b> if there are path-delimiting characters.



