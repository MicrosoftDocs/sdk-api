---
UID: NF:pathcch.PathCchCombine
title: PathCchCombine function
author: windows-sdk-content
description: Combines two path fragments into a single path.
old-location: shell\PathCchCombine.htm
old-project: shell
ms.assetid: 506a4165-f572-4521-958f-56a0296f9c05
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: PathCchCombine, PathCchCombine function [Windows Shell], pathcch/PathCchCombine, shell.PathCchCombine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
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
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# PathCchCombine function


## -description



Combines two path fragments into a single path. This function also canonicalizes any relative path elements, removing "." and ".." elements to simplify the final path.

This function differs from <a href="https://msdn.microsoft.com/798c2e49-04a5-4270-b584-41faf1519e4b">PathCchCombineEx</a> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="https://msdn.microsoft.com/dd619138-f867-4517-bc67-a52c598efad0">PathAllocCombine</a> in that the caller must declare the size of the returned string, which is stored on the stack.

This function differs from <a href="https://msdn.microsoft.com/ed03334b-f688-4993-9685-092135ca29c9">PathCombine</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, <a href="https://msdn.microsoft.com/798c2e49-04a5-4270-b584-41faf1519e4b">PathCchCombineEx</a>, or <a href="https://msdn.microsoft.com/dd619138-f867-4517-bc67-a52c598efad0">PathAllocCombine</a> should be used in place of <a href="https://msdn.microsoft.com/ed03334b-f688-4993-9685-092135ca29c9">PathCombine</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPathOut [out]

A pointer to a buffer that, when this function returns successfully, receives the combined path string. This parameter can point to the same buffer as <i>pszPathIn</i> or <i>pszMore</i>.


### -param cchPathOut [in]

The size of the buffer pointed to by <i>pszPathOut</i>, in characters.


### -param pszPathIn [in, optional]

A pointer to the first path string. This value can be <b>NULL</b>.


### -param pszMore [in, optional]

A pointer to the second path string. If this path begins with a single backslash, it is combined with only the root of the path pointed to by <i>pszPathIn</i>. If this path is fully qualfied, it is copied directly to the output buffer without being combined with the other path. This value can be <b>NULL</b>.


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
This value can be caused by several things, such as the <i>pszPathOut</i> param being set to <b>NULL</b>, or the <i>cchPathOut</i> value being set to 0 or a value greater than PATHCCH_MAX_CCH.

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
The size of one or both of the original paths exceeded PATHCCH_MAX_CCH.

</td>
</tr>
</table>
 




## -remarks



If both <i>pszPathIn</i> and <i>pszMore</i> are <b>NULL</b> or point to empty strings, a single backslash is copied to the buffer pointed to by <i>pszPathOut</i>.




## -see-also




<a href="https://msdn.microsoft.com/25ff08b2-5978-4d44-9877-ba4230ef7d12">PathCchCanonicalize</a>



<a href="https://msdn.microsoft.com/fd7b8ce0-3c67-48fb-8e7e-521a6b438676">PathCchCanonicalizeEx</a>



<a href="https://msdn.microsoft.com/798c2e49-04a5-4270-b584-41faf1519e4b">PathCchCombineEx</a>
 

 

