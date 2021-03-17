---
UID: NF:pathcch.PathCchRemoveBackslashEx
title: PathCchRemoveBackslashEx function (pathcch.h)
description: Removes the trailing backslash from the end of a path string.This function differs from PathCchRemoveBackslash in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.This function differs from PathRemoveBackslash in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PathCchRemoveBackslashEx","PathCchRemoveBackslashEx function [Windows Shell]","pathcch/PathCchRemoveBackslashEx","shell.PathCchRemoveBackslashEx"]
old-location: shell\PathCchRemoveBackslashEx.htm
tech.root: shell
ms.assetid: 250c2faa-94bb-42c1-97d4-37f8f59dbde6
ms.date: 12/05/2018
ms.keywords: PathCchRemoveBackslashEx, PathCchRemoveBackslashEx function [Windows Shell], pathcch/PathCchRemoveBackslashEx, shell.PathCchRemoveBackslashEx
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
 - PathCchRemoveBackslashEx
 - pathcch/PathCchRemoveBackslashEx
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
 - PathCchRemoveBackslashEx
---

# PathCchRemoveBackslashEx function


## -description

Removes the trailing backslash from the end of a path string.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash">PathCchRemoveBackslash</a> in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremovebackslasha">PathRemoveBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>  This function, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash">PathCchRemoveBackslash</a>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremovebackslasha">PathRemoveBackslash</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any trailing backslash removed. If no trailing backslash was found, the string is unchanged.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

### -param ppszEnd [out, optional]

A value that, when this function returns successfully, receives the address of a pointer to end of the new string. If the string is a root path such as "C:\", the pointer points to the backslash; otherwise the pointer points to the string's terminating null character.

### -param pcchRemaining [out, optional]

A pointer to a value that, when this function returns successfully, receives the number of unused characters in the destination buffer, including the terminating null character. If the string is a root path such as "C:\", this count includes the backslash in that string.

## -returns

This function returns <b>S_OK</b> if the function was successful, <b>S_FALSE</b> if the string was a root path or if no backslash was found, or an error code otherwise.

## -remarks

This function will not remove the backslash from a root path string, such as "C:\".