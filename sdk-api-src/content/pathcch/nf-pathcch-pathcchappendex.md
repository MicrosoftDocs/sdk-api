---
UID: NF:pathcch.PathCchAppendEx
title: PathCchAppendEx function (pathcch.h)
description: Appends one path to the end of another.This function differs from PathCchAppend in that it allows for a longer final path to be constructed.This function differs from PathAppend in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PATHCCH_ALLOW_LONG_PATHS","PATHCCH_DO_NOT_NORMALIZE_SEGMENTS","PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH","PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS","PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS","PATHCCH_NONE","PathCchAppendEx","PathCchAppendEx function [Windows Shell]","pathcch/PathCchAppendEx","shell.PathCchAppendEx"]
old-location: shell\PathCchAppendEx.htm
tech.root: shell
ms.assetid: 5421c666-1c8a-4ae8-baba-9e6f69c877df
ms.date: 12/05/2018
ms.keywords: PATHCCH_ALLOW_LONG_PATHS, PATHCCH_DO_NOT_NORMALIZE_SEGMENTS, PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH, PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS, PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS, PATHCCH_NONE, PathCchAppendEx, PathCchAppendEx function [Windows Shell], pathcch/PathCchAppendEx, shell.PathCchAppendEx
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
 - PathCchAppendEx
 - pathcch/PathCchAppendEx
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
 - PathCchAppendEx
---

# PathCchAppendEx function


## -description

Appends one path to the end of another.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend">PathCchAppend</a> in that it allows for a longer final path to be constructed.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathappenda">PathAppend</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b> This function, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend">PathCchAppend</a>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathappenda">PathAppend</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to a buffer that, on entry, contains the original path. When this function returns successfully, the buffer contains the original path plus the appended path.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

### -param pszMore [in, optional]

A pointer the path to append to the end of the path pointed to by <i>pszPath</i>. UNC paths and paths that begin with the sequence \\?\ are accepted and recognized as fully-qualified paths. These paths replace the string pointed to by <i>pszPath</i> instead of being appended to it.

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
<td width="60%">Do not allow for the construction of \\?\ paths (ie, long paths) longer than <b>MAX_PATH</b>. 
</td>
</tr>
<tr>
<td width="40%"><a id="PATHCCH_ALLOW_LONG_PATHS"></a><a id="pathcch_allow_long_paths"></a><dl>
<dt><b>PATHCCH_ALLOW_LONG_PATHS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">Allow the building of \\?\ paths longer than <b>MAX_PATH</b>.
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

<b>Note</b> This value is available starting in Windows 10, version 1703.
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
</table>

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> code, including the following. 

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
Either <i>pszPath</i> or <i>pszMore</i> is <b>NULL</b>, <i>cchPath</i> is 0, or <i>cchPath</i> is greater than <b>PATHCCH_MAX_CCH</b>.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PATHCCH_E_FILENAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The resulting string would exceed <b>PATHCCH_MAX_CCH</b>.
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

This function inserts a backslash between the two strings, if one is not already present.

## -see-also

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend">PathCchAppend</a>