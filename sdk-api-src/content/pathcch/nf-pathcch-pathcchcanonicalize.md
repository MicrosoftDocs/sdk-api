---
UID: NF:pathcch.PathCchCanonicalize
title: PathCchCanonicalize function (pathcch.h)
author: windows-sdk-content
description: Converts a path string into a canonical form.This function differs from PathCchCanonicalizeEx in that you are restricted to a final path of length MAX_PATH.This function differs from PathAllocCanonicalize in that the caller must declare the size of the returned string, which is stored on the stack.This function differs from PathCanonicalize in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchCanonicalize.htm
tech.root: shell
ms.assetid: 25ff08b2-5978-4d44-9877-ba4230ef7d12
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PathCchCanonicalize, PathCchCanonicalize function [Windows Shell], pathcch/PathCchCanonicalize, shell.PathCchCanonicalize
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
 - PathCchCanonicalize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathCchCanonicalize function


## -description



Converts a path string into a canonical form.

This function differs from <a href="https://msdn.microsoft.com/fd7b8ce0-3c67-48fb-8e7e-521a6b438676">PathCchCanonicalizeEx</a> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="https://msdn.microsoft.com/3179fe78-a969-4ee2-a50b-5f4f7d4dad71">PathAllocCanonicalize</a> in that the caller must declare the size of the returned string, which is stored on the stack.

This function differs from <a href="https://msdn.microsoft.com/e9b1e877-2cd6-4dd9-a15b-676cb940daed">PathCanonicalize</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, <a href="https://msdn.microsoft.com/fd7b8ce0-3c67-48fb-8e7e-521a6b438676">PathCchCanonicalizeEx</a>, or <a href="https://msdn.microsoft.com/3179fe78-a969-4ee2-a50b-5f4f7d4dad71">PathAllocCanonicalize</a> should be used in place of <a href="https://msdn.microsoft.com/e9b1e877-2cd6-4dd9-a15b-676cb940daed">PathCanonicalize</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPathOut [out]

A pointer to a buffer that, when this function returns successfully, receives the canonicalized path string.


### -param cchPathOut [in]

The size of the buffer pointed to by <i>pszPathOut</i>, in characters.


### -param pszPathIn [in]

A pointer to the original path string. If this value points to an empty string, or results in an empty string once the "." and ".." elements are removed, a single backslash is copied to the buffer pointed to by <i>pszPathOut</i>.


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
The <i>cchPathOut</i> value is greater than PATHCCH_MAX_CCH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PATHCCH_E_FILENAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
A path segment exceeds the standard path segment length limit of 256 characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate a buffer of the neccessary size.

</td>
</tr>
</table>
 




## -remarks



This function responds to the strings "." and ".." embedded in a path. The ".." string indicates to remove the immediately preceding path segment. The "." string indicates to skip over the next path segment. Note that the root segment of the path cannot be removed. If there are more ".." strings than there are path segments, the function returns S_OK and the buffer pointed to by <i>pszPathOut</i> contains a single backslash, "\".

All trailing periods are removed from the path, except when preceded by the "*" wild card character. In that case, a single period is retained after the '*' character, but all other trailing periods are removed.

If the resulting path is a root drive ("x:"), a backslash is appended ("x:\").

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




<a href="https://msdn.microsoft.com/fd7b8ce0-3c67-48fb-8e7e-521a6b438676">PathCchCanonicalizeEx</a>
 

 

