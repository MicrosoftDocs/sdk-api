---
UID: NF:pathcch.PathAllocCanonicalize
title: PathAllocCanonicalize function (pathcch.h)
description: Converts a path string into a canonical form.This function differs from PathCchCanonicalize and PathCchCanonicalizeEx in that it returns the result on the heap.
helpviewer_keywords: ["PATHCCH_ALLOW_LONG_PATHS","PATHCCH_DO_NOT_NORMALIZE_SEGMENTS","PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH","PATHCCH_ENSURE_TRAILING_SLASH","PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS","PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS","PATHCCH_NONE","PathAllocCanonicalize","PathAllocCanonicalize function [Windows Shell]","pathcch/PathAllocCanonicalize","shell.PathAllocCanonicalize"]
old-location: shell\PathAllocCanonicalize.htm
tech.root: shell
ms.assetid: 3179fe78-a969-4ee2-a50b-5f4f7d4dad71
ms.date: 12/05/2018
ms.keywords: PATHCCH_ALLOW_LONG_PATHS, PATHCCH_DO_NOT_NORMALIZE_SEGMENTS, PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH, PATHCCH_ENSURE_TRAILING_SLASH, PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS, PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS, PATHCCH_NONE, PathAllocCanonicalize, PathAllocCanonicalize function [Windows Shell], pathcch/PathAllocCanonicalize, shell.PathAllocCanonicalize
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
 - PathAllocCanonicalize
 - pathcch/PathAllocCanonicalize
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
 - PathAllocCanonicalize
---

# PathAllocCanonicalize function


## -description

Converts a path string into a canonical form.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a> and <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex">PathCchCanonicalizeEx</a> in that it returns the result on the heap. This means that the caller does not have to declare the size of the returned string and reduces stack use.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcanonicalizea">PathCanonicalize</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b> This function, <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a>, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex">PathCchCanonicalizeEx</a>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcanonicalizea">PathCanonicalize</a>.</div>

## -parameters

### -param pszPathIn [in]

A pointer to a buffer that contains the original string. This value cannot be <b>NULL</b>.

### -param dwFlags [in]

One or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_NONE"></a><a id="____pathcch_none"></a><dl>
<dt><b>PATHCCH_NONE</b></dt>
<dt>0x0000000</dt>
</dl>
</td>
<td width="60%">Do not allow for the construction of \\?\ paths (ie, long paths) longer than <b>MAX_PATH</b> .
</td>
</tr>
<tr>
<td width="40%"><a id="PATHCCH_ALLOW_LONG_PATHS"></a><a id="pathcch_allow_long_paths"></a><dl>
<dt><b>PATHCCH_ALLOW_LONG_PATHS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">Allow the building of \\?\ paths longer than <b>MAX_PATH</b> .
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_enable_long_name_process"></a><dl>
<dt><b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">Forces the API to treat the caller as long path enabled, independent of the process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_disable_long_name_process"></a><dl>
<dt><b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">Forces the API to treat the caller as long path disabled, independent of the process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_DO_NOT_NORMALIZE_SEGMENTS"></a><a id="____pathcch_do_not_normalize_segments"></a><dl>
<dt><b>PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">Disables the normalization of path segments that includes removing trailing dots and spaces. This enables access to paths that win32 path normalization will block.

<b>Note</b>  This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="________PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH"></a><a id="________pathcch_ensure_is_extended_length_path"></a><dl>
<dt><b>PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">Converts the input path into the extended length DOS device path form (with the \\?\ prefix) if not already in that form. This enables access to paths that are otherwise not addressable due to Win32 normalization rules (that can strip trailing dots and spaces) and path length limitations. This option implies the same behavior of <b>PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_ENSURE_TRAILING_SLASH"></a><a id="____pathcch_ensure_trailing_slash"></a><dl>
<dt><b>PATHCCH_ENSURE_TRAILING_SLASH</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">When combining or normalizing a path, ensure there is a trailing backslash.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_CANONICALIZE_SLASHES"></a><a id="____pathcch_canonicalize_slashes"></a><dl>
<dt><b>PATHCCH_CANONICALIZE_SLASHES</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">Convert forward slashes to back slashes and collapse multiple slashes.

<b>Note</b> This value is available starting in Windows 11 (SDK version 10.0.22000.194).
</td>
</tr>
</table>

### -param ppszPathOut [out]

The address of a pointer to a buffer that, when this function returns successfully, receives the canonicalized path string. It is the responsibility of the caller to free this resource, when it is no longer needed, by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function. This value cannot be <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function supports these alternate path forms:

<ul>
<li>\\?\</li>
<li>\\?\\UNC\</li>
<li>\\?\Volume{guid}\</li>
</ul>

This function does not convert forward slashes (/) into back slashes (\\). With untrusted input, this function by itself, cannot be used to convert paths into a form that can be compared with other paths for sub-path or identity. Callers that need that ability should convert forward to back slashes before using this function.
