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

# CHString::CompareNoCase


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CompareNoCase</b> method uses the _wcsicmp function to compare a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string with another string.


## -parameters




### -param lpsz

The other string used for comparison.


## -returns



The <b>CompareNoCase</b> method returns the following values.




## -remarks



The <b>CompareNoCase</b> method, which performs a case-insensitive comparison of the strings, is not affected by locale.


#### Examples

The following code  example shows the use of <b>CHstring::CompareNoCase</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString s1( L"abc" );
CHString s2( L"ABD" );

// Compare with a CHString.
assert( s1.CompareNoCase( s2 ) == 0 );
// Compare with LPCWSTR string.
assert( s1.CompareNoCase( L"ABE" ) &lt; 0 );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/b6c88b83-a369-4cb2-9297-df9c5911d08f">CHString::Collate</a>



<a href="https://msdn.microsoft.com/6e587dd3-b3ae-4afa-9582-b3867d2fb7ef">CHString::Compare</a>
 

 

