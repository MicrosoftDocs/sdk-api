---
UID: NF:pathcch.PathCchCombineEx
title: PathCchCombineEx function (pathcch.h)
description: Combines two path fragments into a single path. (PathCchCombineEx)
helpviewer_keywords: ["PATHCCH_ALLOW_LONG_PATHS","PATHCCH_DO_NOT_NORMALIZE_SEGMENTS","PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH","PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS","PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS","PATHCCH_NONE","PathCchCombineEx","PathCchCombineEx function [Windows Shell]","pathcch/PathCchCombineEx","shell.PathCchCombineEx"]
old-location: shell\PathCchCombineEx.htm
tech.root: shell
ms.assetid: 798c2e49-04a5-4270-b584-41faf1519e4b
ms.date: 12/05/2018
ms.keywords: PATHCCH_ALLOW_LONG_PATHS, PATHCCH_DO_NOT_NORMALIZE_SEGMENTS, PATHCCH_ENSURE_IS_EXTENDED_LENGTH_PATH, PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS, PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS, PATHCCH_NONE, PathCchCombineEx, PathCchCombineEx function [Windows Shell], pathcch/PathCchCombineEx, shell.PathCchCombineEx
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
 - PathCchCombineEx
 - pathcch/PathCchCombineEx
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
 - PathCchCombineEx
---

# PathCchCombineEx function


## -description

Combines two path fragments into a single path. This function also canonicalizes any relative path elements, removing "." and ".." elements to simplify the final path.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine">PathCchCombine</a> in that it allows for a longer final path to be constructed.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine">PathAllocCombine</a> in that the caller must declare the size of the returned string, which is stored on the stack.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcombinea">PathCombine</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b> This function, <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine">PathCchCombine</a>, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine">PathAllocCombine</a> should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcombinea">PathCombine</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPathOut [out]

A pointer to a buffer that, when this function returns successfully, receives the combined path string. This parameter can point to the same buffer as <i>pszPathIn</i> or <i>pszMore</i>.

### -param cchPathOut [in]

The size of the buffer pointed to by <i>pszPathOut</i>, in characters.

### -param pszPathIn [in, optional]

A pointer to the first path string. This value can be <b>NULL</b>.

### -param pszMore [in, optional]

A pointer to the second path string. If this path begins with a single backslash, it is combined with only the root of the path pointed to by <i>pszPathIn</i>. If this path is fully qualified, it is copied directly to the output buffer without being combined with the other path. This value can be <b>NULL</b>.

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
Allow the construction of \\?\ paths longer than <b>MAX_PATH</b>. Note that <i>cchPathOut</i> must be greater than <b>MAX_PATH</b>. If it is not, this flag is ignored.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_enable_long_name_process"></a><dl>
<dt><b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">Forces the API to treat the caller as long path enabled, independent of the process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS"></a><a id="____pathcch_force_disable_long_name_process"></a><dl>
<dt><b>PATHCCH_FORCE_DISABLE_LONG_NAME_PROCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">Forces the API to treat the caller as long path disabled, independent of the process's long name enabled state. This option can be used only when <b>PATHCCH_ALLOW_LONG_PATHS</b> is specified, and cannot be used with <b>PATHCCH_FORCE_ENABLE_LONG_NAME_PROCESS</b>.

<b>Note</b> This value is available starting in Windows 10, version 1703.
</td>
</tr>
<tr>
<td width="40%"><a id="____PATHCCH_DO_NOT_NORMALIZE_SEGMENTS"></a><a id="____pathcch_do_not_normalize_segments"></a><dl>
<dt><b>PATHCCH_DO_NOT_NORMALIZE_SEGMENTS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">Disables the normalization of path segments that includes removing trailing dots and spaces. This enables access to paths that win32 path normalization will block.

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
</table>

## -returns

This function returns an <b>HRESULT</b> code, including the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded. Note that this also includes the case of an empty extension, such as a period with no characters following it. In that case, the original string is returned unaltered.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
This value can be caused by several things, such as the <i>pszPathOut</i> param being set to <b>NULL</b>, or the <i>cchPathOut</i> value being set to 0 or a value greater than <b>PATHCCH_MAX_CCH</b> .
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate enough memory to perform the operation.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PATHCCH_E_FILENAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The size of one or both of the original paths exceeded <b>PATHCCH_MAX_CCH</b> .
</td>
</tr>
</table>

## -remarks

If both <i>pszPathIn</i> and <i>pszMore</i> are <b>NULL</b> or point to empty strings, a single backslash is copied to the buffer pointed to by <i>pszPathOut</i>.

## -see-also

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a>

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex">PathCchCanonicalizeEx</a>

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine">PathCchCombine</a>
