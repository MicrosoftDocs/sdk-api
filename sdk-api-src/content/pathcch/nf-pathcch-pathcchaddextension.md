---
UID: NF:pathcch.PathCchAddExtension
title: PathCchAddExtension function
author: windows-sdk-content
description: Adds a file name extension to a path string.This function differs from PathAddExtension in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchAddExtension.htm
tech.root: shell
ms.assetid: c37b438b-39e7-4f24-b076-2401900dab71
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PathCchAddExtension, PathCchAddExtension function [Windows Shell], pathcch/PathCchAddExtension, shell.PathCchAddExtension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - PathCchAddExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathCchAddExtension function


## -description



Adds a file name extension to a path string.

This function differs from <a href="https://msdn.microsoft.com/2c113d11-11d5-4362-bad5-c859d65aca2a">PathAddExtension</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/2c113d11-11d5-4362-bad5-c859d65aca2a">PathAddExtension</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the buffer contains the string with the appended extension. This value should not be <b>NULL</b>.

                        

<div class="alert"><b>Note</b>  If the original string already has a file name extension present, no new extension will be added and the original string will be unchanged.</div>
<div> </div>

### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


### -param pszExt [in]

A pointer to the file name extension string. This string can be given either with or without a preceding period (".ext" or "ext").


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
This value can be caused by several things, such as the <i>pszPath</i> param being set to <b>NULL</b>, the <i>cchPath</i> being set to 0 or a value greater than PATHCCH_MAX_CCH, or the extension string containing illegal characters or otherwise not being a valid extension.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The original string already has an extension.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PATHCCH_E_FILENAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to hold the returned string.

</td>
</tr>
</table>
 



