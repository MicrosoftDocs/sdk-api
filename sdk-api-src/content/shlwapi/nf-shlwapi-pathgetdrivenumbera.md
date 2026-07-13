---
UID: NF:shlwapi.PathGetDriveNumberA
title: PathGetDriveNumberA function (shlwapi.h)
description: Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number. (ANSI)
helpviewer_keywords: ["PathGetDriveNumberA", "shlwapi/PathGetDriveNumberA"]
old-location: shell\PathGetDriveNumber.htm
tech.root: shell
ms.assetid: 38914866-fdd4-47f2-b0e7-d09d1cfb0eee
ms.date: 12/05/2018
ms.keywords: PathGetDriveNumber, PathGetDriveNumber function [Windows Shell], PathGetDriveNumberA, PathGetDriveNumberW, _win32_PathGetDriveNumber, shell.PathGetDriveNumber, shlwapi/PathGetDriveNumber, shlwapi/PathGetDriveNumberA, shlwapi/PathGetDriveNumberW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathGetDriveNumberA
 - shlwapi/PathGetDriveNumberA
dev_langs:
 - c++
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

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathGetDriveNumber as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

