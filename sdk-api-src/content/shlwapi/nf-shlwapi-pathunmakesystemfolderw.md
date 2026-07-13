---
UID: NF:shlwapi.PathUnmakeSystemFolderW
title: PathUnmakeSystemFolderW function (shlwapi.h)
description: Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system. (Unicode)
helpviewer_keywords: ["PathUnmakeSystemFolder", "PathUnmakeSystemFolder function [Windows Shell]", "PathUnmakeSystemFolderW", "_win32_PathUnmakeSystemFolder", "shell.PathUnmakeSystemFolder", "shlwapi/PathUnmakeSystemFolder", "shlwapi/PathUnmakeSystemFolderW"]
old-location: shell\PathUnmakeSystemFolder.htm
tech.root: shell
ms.assetid: 9c748ed6-3ee6-4889-8fdd-b33ed9d711d0
ms.date: 12/05/2018
ms.keywords: PathUnmakeSystemFolder, PathUnmakeSystemFolder function [Windows Shell], PathUnmakeSystemFolderA, PathUnmakeSystemFolderW, _win32_PathUnmakeSystemFolder, shell.PathUnmakeSystemFolder, shlwapi/PathUnmakeSystemFolder, shlwapi/PathUnmakeSystemFolderA, shlwapi/PathUnmakeSystemFolderW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathUnmakeSystemFolderW (Unicode) and PathUnmakeSystemFolderA (ANSI)
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
 - PathUnmakeSystemFolderW
 - shlwapi/PathUnmakeSystemFolderW
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
 - PathUnmakeSystemFolder
 - PathUnmakeSystemFolderA
 - PathUnmakeSystemFolderW
---

# PathUnmakeSystemFolderW function


## -description

Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system.

## -parameters

### -param pszPath [in]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the name of an existing folder that will have the system folder attributes removed.

## -returns

Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

## -remarks

> [!NOTE]
> The shlwapi.h header defines PathUnmakeSystemFolder as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

