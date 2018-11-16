---
UID: NF:shlwapi.PathUnmakeSystemFolderA
title: PathUnmakeSystemFolderA function
author: windows-sdk-content
description: Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system.
old-location: shell\PathUnmakeSystemFolder.htm
tech.root: shell
ms.assetid: 9c748ed6-3ee6-4889-8fdd-b33ed9d711d0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PathUnmakeSystemFolder, PathUnmakeSystemFolder function [Windows Shell], PathUnmakeSystemFolderA, PathUnmakeSystemFolderW, _win32_PathUnmakeSystemFolder, shell.PathUnmakeSystemFolder, shlwapi/PathUnmakeSystemFolder, shlwapi/PathUnmakeSystemFolderA, shlwapi/PathUnmakeSystemFolderW
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
req.unicode-ansi: PathUnmakeSystemFolderW (Unicode) and PathUnmakeSystemFolderA (ANSI)
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
api_name:
 - PathUnmakeSystemFolder
 - PathUnmakeSystemFolderA
 - PathUnmakeSystemFolderW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PathUnmakeSystemFolderA
: 
---

# PathUnmakeSystemFolderA function


## -description


Removes the attributes from a folder that make it a system folder. This folder must actually exist in the file system.


## -parameters




### -param pszPath [in]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the name of an existing folder that will have the system folder attributes removed.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.



