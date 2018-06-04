---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PathMatchSpecExA function


## -description


Matches a file name from a path against one or more file name patterns.


## -parameters




### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path from which the file name to be matched is taken.


### -param pszSpec [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file name pattern for which to search. This can be the exact name, or it can contain wildcard characters. If exactly one pattern is specified, set the <b>PMSF_NORMAL</b> flag in <i>dwFlags</i>. If more than one pattern is specified, separate them with semicolons and set the <b>PMSF_MULTIPLE</b> flag.


### -param dwFlags [in]

Type: <b>DWORD</b>

Modifies the search condition. The following are valid flags.



#### PMSF_NORMAL (0x00000000)

The <i>pszSpec</i> parameter points to a single file name pattern to be matched.



#### PMSF_MULTIPLE (0x00000001)

The <i>pszSpec</i> parameter points to a semicolon-delimited list of file name patterns to be matched.



#### PMSF_DONT_STRIP_SPACES (0x00010000)

If <b>PMSF_NORMAL</b> is used, ignore leading spaces in the string pointed to by <i>pszSpec</i>. If <b>PMSF_MULTIPLE</b> is used, ignore leading spaces in each file type contained in the string pointed to by <i>pszSpec</i>. This flag can be combined with <b>PMSF_NORMAL</b> and <b>PMSF_MULTIPLE</b>.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

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
A file name pattern specified in <i>pszSpec</i> matched the file name found in the string pointed to by <i>pszFile</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No file name pattern specified in <i>pszSpec</i> matched the file name found in the string pointed to by <i>pszFile</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/908e7204-d168-4179-9c7b-ad46ba68bebc">PathMatchSpec</a>
 

 

