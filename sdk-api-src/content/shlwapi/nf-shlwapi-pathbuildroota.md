---
UID: NF:shlwapi.PathBuildRootA
title: PathBuildRootA function (shlwapi.h)
description: Creates a root path from a given drive number. (ANSI)
helpviewer_keywords: ["PathBuildRootA", "shlwapi/PathBuildRootA"]
old-location: shell\PathBuildRoot.htm
tech.root: shell
ms.assetid: 0a6895bd-54cf-499c-9057-f2d721bce5d9
ms.date: 12/05/2018
ms.keywords: PathBuildRoot, PathBuildRoot function [Windows Shell], PathBuildRootA, PathBuildRootW, _win32_PathBuildRoot, shell.PathBuildRoot, shlwapi/PathBuildRoot, shlwapi/PathBuildRootA, shlwapi/PathBuildRootW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathBuildRootW (Unicode) and PathBuildRootA (ANSI)
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
 - PathBuildRootA
 - shlwapi/PathBuildRootA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - PathBuildRoot
 - PathBuildRootA
 - PathBuildRootW
---

# PathBuildRootA function


## -description

Creates a root path from a given drive number.

## -parameters

### -param pszRoot [out]

Type: <b>LPTSTR</b>

A pointer to the string that receives the constructed root path. This buffer must be at least four characters in size.

### -param iDrive [in]

Type: <b>int</b>

A variable of type <b>int</b> that indicates the desired drive number. It should be between 0 and 25.

## -returns

Type: <b>LPTSTR</b>

Returns the address of the constructed root path. If the call fails for any reason (for example, an invalid drive number), <i>szRoot</i> is returned unchanged.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathBuildRoot as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

