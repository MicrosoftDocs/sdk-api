---
UID: NF:pathcch.PathCchAppend
title: PathCchAppend function (pathcch.h)
description: Appends one path to the end of another.This function differs from PathCchAppendEx in that you are restricted to a final path of length MAX_PATH.This function differs from PathAppend in that it accepts paths with &quot;\\&quot;, &quot;\\?\&quot; and &quot;\\?\UNC\&quot; prefixes.
helpviewer_keywords: ["PathCchAppend","PathCchAppend function [Windows Shell]","pathcch/PathCchAppend","shell.PathCchAppend"]
old-location: shell\PathCchAppend.htm
tech.root: shell
ms.assetid: b64884ad-15c7-495e-8037-34daf68f8cf7
ms.date: 12/05/2018
ms.keywords: PathCchAppend, PathCchAppend function [Windows Shell], pathcch/PathCchAppend, shell.PathCchAppend
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
 - PathCchAppend
 - pathcch/PathCchAppend
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
 - PathCchAppend
---

# PathCchAppend function


## -description

Appends one path to the end of another.

This function differs from <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex">PathCchAppendEx</a> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathappenda">PathAppend</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>  This function, or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex">PathCchAppendEx</a>, should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathappenda">PathAppend</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to a buffer that, on entry, contains the original path. When this function returns successfully, the buffer contains the original path plus the appended path.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

### -param pszMore [in, optional]

A pointer to the path to append to the end of the path pointed to by <i>pszPath</i>. UNC paths and paths beginning with the "\\?\" sequence are accepted and recognized as fully-qualified paths. These paths replace the string pointed to by <i>pszPath</i> instead of being appended to it.

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

<a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex">PathCchAppendEx</a>