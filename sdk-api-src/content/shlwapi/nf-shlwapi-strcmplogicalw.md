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

# StrCmpLogicalW function


## -description


Compares two Unicode strings. Digits in the strings are considered as numerical content rather than text. This test is not case-sensitive.


## -parameters




### -param psz1 [in]

Type: <b>PCWSTR</b>

A pointer to the first null-terminated string to be compared.


### -param psz2 [in]

Type: <b>PCWSTR</b>

A pointer to the second null-terminated string to be compared.


## -returns



Type: <b>int</b>

<ul>
<li>Returns zero if the strings are identical.</li>
<li>Returns 1 if the string pointed to by <i>psz1</i> has a greater value than that pointed to by <i>psz2</i>.</li>
<li>Returns -1 if the string pointed to by <i>psz1</i> has a lesser value than that pointed to by <i>psz2</i>.</li>
</ul>



## -remarks



This function's ordering schema differs somewhat from <a href="https://msdn.microsoft.com/d059b6bd-8f03-4273-aa7a-b8b07f84d268">StrCmpI</a>, which also compares strings without regard to case sensitivity. Considering digits by their numerical value—as <b>StrCmpLogicalW</b> does—strings are ordered as follows:
		
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>2string
3string
20string
st2ring
st3ring
st20ring
string2
string3
string20</pre>
</td>
</tr>
</table></span></div>
<b>StrCmpI</b> considers digits in the string only as text so that those same strings are ordered as follows:
		    
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>20string
2string
3string
st20ring
st2ring
st3ring
string2
string20
string3</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  Behavior of this function, and therefore the results it returns, can change from release to release. It should not be used for canonical sorting applications.</div>
<div> </div>


