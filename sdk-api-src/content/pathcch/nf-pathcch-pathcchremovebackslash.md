---
UID: NF:pathcch.PathCchRemoveBackslash
title: PathCchRemoveBackslash function (pathcch.h)
description: Removes the trailing backslash from the end of a path string.This function differs from PathRemoveBackslash in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PathCchRemoveBackslash","PathCchRemoveBackslash function [Windows Shell]","pathcch/PathCchRemoveBackslash","shell.PathCchRemoveBackslash"]
old-location: shell\PathCchRemoveBackslash.htm
tech.root: shell
ms.assetid: 61afc20e-ee6c-46ad-a058-64c57de41ba4
ms.date: 12/05/2018
ms.keywords: PathCchRemoveBackslash, PathCchRemoveBackslash function [Windows Shell], pathcch/PathCchRemoveBackslash, shell.PathCchRemoveBackslash
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
 - PathCchRemoveBackslash
 - pathcch/PathCchRemoveBackslash
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
 - PathCchRemoveBackslash
---

# PathCchRemoveBackslash function


## -description

Removes the trailing backslash from the end of a path string.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremovebackslasha">PathRemoveBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>  This function, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex">PathCchRemoveBackslashEx</a>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremovebackslasha">PathRemoveBackslash</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any trailing backslash removed. If no trailing backslash was found, the string is unchanged.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

## -returns

This function returns <b>S_OK</b> if the function was successful, <b>S_FALSE</b> if the string was a root path or if no backslash was found, or an error code otherwise.

## -remarks

This function will not remove the backslash from a root path string, such as "C:\".