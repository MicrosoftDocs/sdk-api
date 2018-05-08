---
UID: NF:shlwapi.PathAddBackslashW
title: PathAddBackslashW function
author: windows-driver-content
description: Adds a backslash to the end of a string to create the correct syntax for a path.
old-location: shell\PathAddBackslash.htm
old-project: shell
ms.assetid: 27d8aec7-8b00-412a-9a42-8ce27e262781
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: PathAddBackslash, PathAddBackslash function [Windows Shell], PathAddBackslashA, PathAddBackslashW, _win32_PathAddBackslash, shell.PathAddBackslash, shlwapi/PathAddBackslash, shlwapi/PathAddBackslashA, shlwapi/PathAddBackslashW
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
req.unicode-ansi: PathAddBackslashW (Unicode) and PathAddBackslashA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
-	PathAddBackslash
-	PathAddBackslashA
-	PathAddBackslashW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathAddBackslashW function


## -description


Adds a backslash to the end of a string to create the correct syntax for a path. If the source path already has a trailing backslash, no backslash will be added.

            
<div class="alert"><b>Note</b>  Misuse of this function can lead to a buffer overrun. We recommend the use of the safer <a href="https://msdn.microsoft.com/b50677cd-8815-4d84-b70a-c83863378c56">PathCchAddBackslash</a> or <a href="https://msdn.microsoft.com/89adf45f-f16d-49d1-9e76-b57b73b4d4c3">PathCchAddBackslashEx</a> function in its place.</div><div> </div>

## -parameters




### -param pszPath

TBD




#### - lpszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a buffer with a string that represents a path. The size of this buffer must be set to MAX_PATH to ensure that it is large enough to hold the returned string.


## -returns



Type: <b>LPTSTR</b>

A pointer that, when this function returns successfully, points to the new string's terminating null character. If the backslash could not be appended due to inadequate buffer size, this value is <b>NULL</b>.



