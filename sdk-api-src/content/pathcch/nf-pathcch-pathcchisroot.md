---
UID: NF:pathcch.PathCchIsRoot
title: PathCchIsRoot function (pathcch.h)
description: Determines whether a path string refers to the root of a volume.This function differs from PathIsRoot in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchIsRoot.htm
tech.root: shell
ms.assetid: b9770030-b298-47f8-98a7-3ce9b4d44dd1
ms.date: 12/05/2018
ms.keywords: PathCchIsRoot, PathCchIsRoot function [Windows Shell], pathcch/PathCchIsRoot, shell.PathCchIsRoot
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
 - PathCchIsRoot
 - pathcch/PathCchIsRoot
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
 - PathCchIsRoot
---

# PathCchIsRoot function


## -description

Determines whether a path string refers to the root of a volume.

This function differs from <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathisroota">PathIsRoot</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.

## -parameters

### -param pszPath [in, optional]

A pointer to the path string.

## -returns

Returns <b>TRUE</b> if the specified path is a root, or <b>FALSE</b> otherwise.

## -remarks

The following table shows the <b>PathCchIsRoot</b> return value for various paths.
            
                

<table class="clsStd">
<tr>
<th>Path</th>
<th>PathCchIsRoot</th>
</tr>
<tr>
<td>"c:\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"c:"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"c:\path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\path1"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\path1\path2"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\path1\path2\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\path1\path2\path3"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\path1"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\path1\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\path2"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\path2\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\path2\path3"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\UNC\path1"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\UNC\path1\"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\c:\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\c:"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\c:\path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\Volume{guid}\"</td>
<td>TRUE</td>
</tr>
<tr>
<td>"\\?\Volume{guid}"</td>
<td>FALSE</td>
</tr>
<tr>
<td>"\\?\Volume{guid}\path1"</td>
<td>FALSE</td>
</tr>
<tr>
<td>NULL</td>
<td>FALSE</td>
</tr>
<tr>
<td>""</td>
<td>FALSE</td>
</tr>
</table>
 

This function returns <b>TRUE</b> for paths such as "\", "<i>X</i>:\" or "&#92;&#92;<i>server</i>&#92;<i>share</i>". Paths such as "..\path2" or "&#92;&#92;<i>server</i>\" return <b>FALSE</b>.
