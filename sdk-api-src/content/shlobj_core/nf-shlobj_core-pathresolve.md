---
UID: NF:shlobj_core.PathResolve
title: PathResolve function (shlobj_core.h)
description: PathResolve may be altered or unavailable.
helpviewer_keywords: ["PRF_DONTFINDLNK","PRF_FIRSTDIRDEF","PRF_REQUIREABSOLUTE","PRF_TRYPROGRAMEXTENSIONS","PRF_VERIFYEXISTS","PathResolve","PathResolve function [Windows Shell]","_win32_PathResolve","shell.PathResolve","shlobj_core/PathResolve"]
old-location: shell\PathResolve.htm
tech.root: shell
ms.assetid: 84bf0b56-513f-4ac6-b2cf-11f0c471da1e
ms.date: 12/05/2018
ms.keywords: PRF_DONTFINDLNK, PRF_FIRSTDIRDEF, PRF_REQUIREABSOLUTE, PRF_TRYPROGRAMEXTENSIONS, PRF_VERIFYEXISTS, PathResolve, PathResolve function [Windows Shell], _win32_PathResolve, shell.PathResolve, shlobj_core/PathResolve
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathResolve
 - shlobj_core/PathResolve
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - PathResolve
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# PathResolve function


## -description

<p class="CCE_Message">[<b>PathResolve</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Converts a relative or unqualified path name to a fully qualified path name.

## -parameters

### -param pszPath [in, out]

Type: <b>PWSTR</b>

A null-terminated Unicode string that contains the path to resolve. When the function returns, the string contains the corresponding fully qualified path. This buffer should be at least MAX_PATH characters long.

### -param dirs [in, optional]

Type: <b>PZPCWSTR</b>

A pointer to an optional null-terminated array of directories to be searched first in the case that the path cannot be resolved from <i>pszPath</i>. This value can be <b>NULL</b>.

### -param fFlags

Type: <b>UINT</b>

Flags that specify how the function operates.



#### PRF_VERIFYEXISTS

Return <b>TRUE</b> if the file's existence is verified; otherwise <b>FALSE</b>.



#### PRF_TRYPROGRAMEXTENSIONS

Look for the specified path with the following extensions appended: .pif, .com, .bat, .cmd, .lnk, and .exe.



#### PRF_FIRSTDIRDEF

Look first in the directory or directories specified by <i>dirs</i>.



#### PRF_DONTFINDLNK

Ignore .lnk files.



#### PRF_REQUIREABSOLUTE

Require an absolute (full) path.

## -returns

Type: <b>int</b>

Returns <b>TRUE</b>, unless PRF_VERIFYEXISTS is set. If that flag is set, the function returns <b>TRUE</b> if the file is verified to exist and <b>FALSE</b> otherwise. It also sets an ERROR_FILE_NOT_FOUND error code that you can retrieve by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A <b>FALSE</b> return value does not necessarily mean that the file does not exist. It might mean that the function is simply unable to find the file from the supplied information.

If <b>PathResolve</b> cannot resolve the path specified in <i>pszPath</i>, it calls <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathfindonpatha">PathFindOnPath</a> using <i>pszPath</i> and <i>dirs</i> as the parameters.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathfindonpatha">PathFindOnPath</a>
