---
UID: NF:pathcch.PathCchAddBackslashEx
title: PathCchAddBackslashEx function (pathcch.h)
description: Adds a backslash to the end of a string to create the correct syntax for a path. (PathCchAddBackslashEx)
helpviewer_keywords: ["PathCchAddBackslashEx","PathCchAddBackslashEx function [Windows Shell]","pathcch/PathCchAddBackslashEx","shell.PathCchAddBackslashEx"]
old-location: shell\PathCchAddBackslashEx.htm
tech.root: shell
ms.assetid: 89adf45f-f16d-49d1-9e76-b57b73b4d4c3
ms.date: 12/05/2018
ms.keywords: PathCchAddBackslashEx, PathCchAddBackslashEx function [Windows Shell], pathcch/PathCchAddBackslashEx, shell.PathCchAddBackslashEx
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pathcch.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathCchAddBackslashEx
 - pathcch/PathCchAddBackslashEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - pathcch.lib
 - API-MS-Win-Core-Path-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PathCchAddBackslashEx
---

# PathCchAddBackslashEx function


## -description

Adds a backslash to the end of a string to create the correct syntax for a path. If the source path already has a trailing backslash, no backslash will be added.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash">PathCchAddBackslash</a> in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathaddbackslasha">PathAddBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>  This function, or <b><a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash">PathCchAddBackslash</a></b>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathaddbackslasha">PathAddBackslash</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the buffer contains the string with the appended backslash. This value should not be <b>NULL</b>.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

### -param ppszEnd [out, optional]

A value that, when this function returns successfully, receives the address of a pointer to the terminating null character at the end of the string.

### -param pcchRemaining [out, optional]

A pointer to a value that, when this function returns successfully, is set to the number of unused characters in the destination buffer, including the terminating null character.

## -returns

This function returns <b>S_OK</b> if the function was successful, <b>S_FALSE</b> if the path string already ends in a backslash, or an error code otherwise.

## -see-also

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash">PathCchAddBackslash</a>
