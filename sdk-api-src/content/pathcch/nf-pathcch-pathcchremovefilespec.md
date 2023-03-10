---
UID: NF:pathcch.PathCchRemoveFileSpec
title: PathCchRemoveFileSpec function (pathcch.h)
description: Removes the last element in a path string, whether that element is a file name or a directory name.
helpviewer_keywords: ["PathCchRemoveFileSpec","PathCchRemoveFileSpec function [Windows Shell]","pathcch/PathCchRemoveFileSpec","shell.PathCchRemoveFileSpec"]
old-location: shell\PathCchRemoveFileSpec.htm
tech.root: shell
ms.assetid: c37aeddc-ed24-4828-b92b-bce0e6384726
ms.date: 12/05/2018
ms.keywords: PathCchRemoveFileSpec, PathCchRemoveFileSpec function [Windows Shell], pathcch/PathCchRemoveFileSpec, shell.PathCchRemoveFileSpec
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
 - PathCchRemoveFileSpec
 - pathcch/PathCchRemoveFileSpec
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
 - PathCchRemoveFileSpec
---

# PathCchRemoveFileSpec function


## -description

Removes the last element in a path string, whether that element is a file name or a directory name. The element's leading backslash is also removed.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremovefilespeca">PathRemoveFileSpec</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

<div class="alert"><b>Note</b>This function should be used in place of <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathremovefilespeca">PathRemoveFileSpec</a> to prevent the possibility of a buffer overrun.</div>

## -parameters

### -param pszPath [in, out]

A pointer to the fully-qualified path string. When this function returns successfully, the string will have had its last element and its leading backslash removed. This function does not affect root paths such as "C:\". In the case of a root path, the path string is returned unaltered. If a path string ends with a trailing backslash, only that backslash is removed.

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.

## -returns

This function returns <b>S_OK</b> if the function was successful, <b>S_FALSE</b> if there was nothing to remove, or an error code otherwise.

## -remarks

The following table shows the effect of this function on a selection of path strings.

<table class="clsStd">
<tr>
<th>Original String</th>
<th>Returned String</th>
</tr>
<tr>
<td>"C:\path1"</td>
<td>"C:\"</td>
</tr>
<tr>
<td>"C:\path1\path2"</td>
<td>"C:\path1"</td>
</tr>
<tr>
<td>"C:\path1\"</td>
<td>"C:\path1"</td>
</tr>
<tr>
<td>"\\path1\path2\path3"</td>
<td>"\\path1\path2"</td>
</tr>
<tr>
<td>"\path1"</td>
<td>"\"</td>
</tr>
</table>