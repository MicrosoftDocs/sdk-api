---
UID: NF:pathcch.PathCchCombine
title: PathCchCombine function (pathcch.h)
description: Combines two path fragments into a single path. (PathCchCombine)
helpviewer_keywords: ["PathCchCombine","PathCchCombine function [Windows Shell]","pathcch/PathCchCombine","shell.PathCchCombine"]
old-location: shell\PathCchCombine.htm
tech.root: shell
ms.assetid: 506a4165-f572-4521-958f-56a0296f9c05
ms.date: 12/05/2018
ms.keywords: PathCchCombine, PathCchCombine function [Windows Shell], pathcch/PathCchCombine, shell.PathCchCombine
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
 - PathCchCombine
 - pathcch/PathCchCombine
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
 - PathCchCombine
---

# PathCchCombine function


## -description

Combines two path fragments into a single path. This function also canonicalizes any relative path elements, removing "." and ".." elements to simplify the final path.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex">PathCchCombineEx</a> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine">PathAllocCombine</a> in that the caller must declare the size of the returned string, which is stored on the stack.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcombinea">PathCombine</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>  This function, <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex">PathCchCombineEx</a>, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine">PathAllocCombine</a> should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathcombinea">PathCombine</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPathOut [out]

A pointer to a buffer that, when this function returns successfully, receives the combined path string. This parameter can point to the same buffer as <i>pszPathIn</i> or <i>pszMore</i>.

### -param cchPathOut [in]

The size of the buffer pointed to by <i>pszPathOut</i>, in characters.

### -param pszPathIn [in, optional]

A pointer to the first path string. This value can be <b>NULL</b>.

### -param pszMore [in, optional]

A pointer to the second path string. If this path begins with a single backslash, it is combined with only the root of the path pointed to by <i>pszPathIn</i>. If this path is fully qualified, it is copied directly to the output buffer without being combined with the other path. This value can be <b>NULL</b>.

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
This value can be caused by several things, such as the <i>pszPathOut</i> param being set to <b>NULL</b>, or the <i>cchPathOut</i> value being set to 0 or a value greater than <b>PATHCCH_MAX_CCH</b>.
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
The size of one or both of the original paths exceeded <b>PATHCCH_MAX_CCH</b>.
</td>
</tr>
</table>

## -remarks

If both <i>pszPathIn</i> and <i>pszMore</i> are <b>NULL</b> or point to empty strings, a single backslash is copied to the buffer pointed to by <i>pszPathOut</i>.

## -see-also

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize">PathCchCanonicalize</a>

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex">PathCchCanonicalizeEx</a>

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex">PathCchCombineEx</a>
