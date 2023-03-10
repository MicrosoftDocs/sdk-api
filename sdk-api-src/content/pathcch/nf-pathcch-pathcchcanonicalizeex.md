---
UID: NF:pathcch.PathCchCanonicalizeEx
title: PathCchCanonicalizeEx function (pathcch.h)
description: Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.This function differs from PathCchCanonicalize in that it allows for a longer final path to be constructed.This function differs from PathAllocCanonicalize in that the caller must declare the size of the returned string, which is stored on the stack.This function differs from PathCanonicalize in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PATHCCH_ALLOW_LONG_PATHS","PATHCCH_DO_NOT_NORMALIZE_SEGMENTS","PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH","PATHCCH_ENSURE_TRAILING_SLASH","PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS","PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS","PATHCCH_NONE","PathCchCanonicalizeEx","PathCchCanonicalizeEx function [Windows Shell]","pathcch/PathCchCanonicalizeEx","shell.PathCchCanonicalizeEx"]
old-location: shell\PathCchCanonicalizeEx.htm
tech.root: shell
ms.assetid: fd7b8ce0-3c67-48fb-8e7e-521a6b438676
ms.date: 12/05/2018
ms.keywords: PATHCCH_ALLOW_LONG_PATHS, PATHCCH_DO_NOT_NORMALIZE_SEGMENTS, PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH, PATHCCH_ENSURE_TRAILING_SLASH, PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS, PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS, PATHCCH_NONE, PathCchCanonicalizeEx, PathCchCanonicalizeEx function [Windows Shell], pathcch/PathCchCanonicalizeEx, shell.PathCchCanonicalizeEx
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
 - PathCchCanonicalizeEx
 - pathcch/PathCchCanonicalizeEx
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
 - PathCchCanonicalizeEx
---

# PathCchCanonicalizeEx function


## -description

Simplifies a path by removing navigation elements such as "." and ".." to produce a direct, well-formed path.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a> in that it allows for a longer final path to be constructed.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathalloccanonicalize">PathAllocCanonicalize</a> in that the caller must declare the size of the returned string, which is stored on the stack.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcanonicalizea">PathCanonicalize</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b> This function, <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a>, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathalloccanonicalize">PathAllocCanonicalize</a> should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcanonicalizea">PathCanonicalize</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPathOut [out]

A pointer to a buffer that, when this function returns successfully, receives the edited path string.

### -param cchPathOut [in]

The size of the buffer pointed to by <i>pszPathOut</i>, in characters.

### -param pszPathIn [in]

A pointer to the original path string. If this value is <b>NULL</b>, points to an empty string, or results in an empty string once the "." and ".." elements are removed, a single backslash is copied to the buffer pointed to by <i>pszPathOut</i>.

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
<td width="60%">
Do not allow for the construction of \\?\ paths (ie, long paths) longer than <b>MAX_PATH</b> .
</td>
</tr>
<tr>
<td width="40%"><a id="PATHCCH_ALLOW_LONG_PATHS"></a><a id="pathcch_allow_long_paths"></a><dl>
<dt><b>PATHCCH_ALLOW_LONG_PATHS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Allow the building of \\?\ paths longer than <b>MAX_PATH</b> . Note that <i>cchPathOut</i> must be greater than <b>MAX_PATH</b> . If it is not, this flag is ignored.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_enable_long_name_process"></a><dl>
<dt><b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Forces the API to treat the caller as long path enabled, independent of the process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_disable_long_name_process"></a><dl>
<dt><b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Forces the API to treat the caller as long path disabled, independent of the process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_DO_NOT_NORMALIZE_SEGMENTS"></a><a id="____pathcch_do_not_normalize_segments"></a><dl>
<dt><b>PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Disables the normalization of path segments that includes removing trailing dots and spaces. This enables access to paths that win32 path normalization will block.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="________PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH"></a><a id="________pathcch_ensure_is_extended_length_path"></a><dl>
<dt><b>PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">Converts the input path into the extended length DOS device path form (with the \\?\ prefix) if not already in that form. This enables access to paths that are otherwise not addressable due to Win32 normalization rules (that can strip trailing dots and spaces) and path length limitations. This option implies the same behavior of <b>PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
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
</table>

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> code, including but not limited to the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>cchPathOut</i> value is greater than <b>PATHCCH_MAX_CCH</b>.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PATHCCH_E_FILENAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
A path segment has more than <b>PATHCCH_MAX_CCH</b> characters, or, if the <b>PATHCCH_ALLOW_LONG_PATHS</b> flag is not set, exceeds the standard path segment length limit of 256 characters.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate a buffer of the necessary size.
</td>
</tr>
</table>

## -remarks

This function responds to the strings "." and ".." embedded in a path. The ".." string indicates to remove the immediately preceding path segment. The "." string indicates to skip over the next path segment. Note that the root segment of the path cannot be removed. If there are more ".." strings than there are path segments, the function returns <b>S_OK</b> and the buffer pointed to by <i>pszPathOut</i> contains a single backslash, "\\".

All trailing periods are removed from the path, except when preceded by the "*" wild card character. In that case, a single period is retained after the '*' character, but all other trailing periods are removed.

If the resulting path is a root drive ("x:"), a backslash is appended ("x:\\").

This function does not convert forward slashes (/) into back slashes (\\). With untrusted input, this function by itself, cannot be used to convert paths into a form that can be compared with other paths for sub-path or identity. Callers that need that ability should convert forward to back slashes before using this function.

The following examples show the effect of these strings.

<table class="clsStd">
<tr>
<th>Original string</th>
<th>Canonicalized string</th>
</tr>
<tr>
<td>C:\name_1\.\name_2\..\name_3</td>
<td>C:\name_1\name_3</td>
</tr>
<tr>
<td>C:\name_1\..\name_2\.\name_3</td>
<td>C:\name_2\name_3</td>
</tr>
<tr>
<td>C:\name_1\name_2\.\name_3\..\name_4</td>
<td>C:\name_1\name_2\name_4</td>
</tr>
<tr>
<td>C:\name_1\.\name_2\.\name_3\..\name_4\..</td>
<td>C:\name_1\name_2</td>
</tr>
<tr>
<td>C:\name_1\*...</td>
<td>C:\name_1\*.</td>
</tr>
<tr>
<td>C:\..</td>
<td>C:\</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a>