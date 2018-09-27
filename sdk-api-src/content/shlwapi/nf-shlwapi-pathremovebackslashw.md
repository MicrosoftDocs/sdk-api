---
UID: NF:shlwapi.PathRemoveBackslashW
title: PathRemoveBackslashW function
author: windows-sdk-content
description: Removes the trailing backslash from a given path.
old-location: shell\PathRemoveBackslash.htm
tech.root: shell
ms.assetid: 58d13c38-40aa-4aaa-81dc-2b68425f1fe0
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: PathRemoveBackslash, PathRemoveBackslash function [Windows Shell], PathRemoveBackslashA, PathRemoveBackslashW, _win32_PathRemoveBackslash, shell.PathRemoveBackslash, shlwapi/PathRemoveBackslash, shlwapi/PathRemoveBackslashA, shlwapi/PathRemoveBackslashW
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
req.unicode-ansi: PathRemoveBackslashW (Unicode) and PathRemoveBackslashA (ANSI)
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
 - PathRemoveBackslash
 - PathRemoveBackslashA
 - PathRemoveBackslashW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathRemoveBackslashW function


## -description


Removes the trailing backslash from a given path.
<div class="alert"><b>Note</b>  This function is deprecated. We recommend the use of the <a href="https://msdn.microsoft.com/61afc20e-ee6c-46ad-a058-64c57de41ba4">PathCchRemoveBackslash</a> or <a href="https://msdn.microsoft.com/250c2faa-94bb-42c1-97d4-37f8f59dbde6">PathCchRemoveBackslashEx</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH that contains the path from which to remove the backslash.


## -returns



Type: <b>LPTSTR</b>

A pointer that, when this function returns successfully and if a backslash has been removed, points to the terminating null character that has replaced the backslash at the end of the string. If the path did not include a trailing backslash, this value will point to the final character in the string.



