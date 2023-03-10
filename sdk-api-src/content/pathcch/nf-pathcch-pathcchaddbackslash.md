---
UID: NF:pathcch.PathCchAddBackslash
title: PathCchAddBackslash function (pathcch.h)
description: Adds a backslash to the end of a string to create the correct syntax for a path. (PathCchAddBackslash)
helpviewer_keywords: ["PathCchAddBackslash","PathCchAddBackslash function [Windows Shell]","pathcch/PathCchAddBackslash","shell.PathCchAddBackslash"]
old-location: shell\PathCchAddBackslash.htm
tech.root: shell
ms.assetid: b50677cd-8815-4d84-b70a-c83863378c56
ms.date: 12/05/2018
ms.keywords: PathCchAddBackslash, PathCchAddBackslash function [Windows Shell], pathcch/PathCchAddBackslash, shell.PathCchAddBackslash
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
 - PathCchAddBackslash
 - pathcch/PathCchAddBackslash
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
 - PathCchAddBackslash
---

# PathCchAddBackslash function


## -description

Adds a backslash to the end of a string to create the correct syntax for a path. If the source path already has a trailing backslash, no backslash will be added.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex">PathCchAddBackslashEx</a> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathaddbackslasha">PathAddBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>  This function, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex">PathCchAddBackslashEx</a>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathaddbackslasha">PathAddBackslash</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the buffer contains the string with the appended backslash. This value should not be <b>NULL</b>.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

## -returns

This function returns <b>S_OK</b> if the function was successful, <b>S_FALSE</b> if the path string already ends in a backslash, or an error code otherwise.

## -see-also

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex">PathCchAddBackslashEx</a>
