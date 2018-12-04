---
UID: NF:shlwapi.PathGetDriveNumberA
title: PathGetDriveNumberA function
author: windows-sdk-content
description: Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.
old-location: shell\PathGetDriveNumber.htm
tech.root: shell
ms.assetid: 38914866-fdd4-47f2-b0e7-d09d1cfb0eee
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: PathGetDriveNumber, PathGetDriveNumber function [Windows Shell], PathGetDriveNumberA, PathGetDriveNumberW, _win32_PathGetDriveNumber, shell.PathGetDriveNumber, shlwapi/PathGetDriveNumber, shlwapi/PathGetDriveNumberA, shlwapi/PathGetDriveNumberW
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
req.unicode-ansi: PathGetDriveNumberW (Unicode) and PathGetDriveNumberA (ANSI)
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
 - PathGetDriveNumber
 - PathGetDriveNumberA
 - PathGetDriveNumberW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathGetDriveNumberA function


## -description


Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be searched.


## -returns



Type: <b>int</b>

Returns 0 through 25 (corresponding to 'A' through 'Z') if the path has a drive letter, or -1 otherwise.



