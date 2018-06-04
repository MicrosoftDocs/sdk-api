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

# CHString::Find(LPCWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">Find</a> method searches a string for the first match of a substring.


## -parameters




### -param lpszSub

A substring that the method searches for.


## -returns



If the <a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">Find</a> method is successful, it returns the zero-based index of the first character in this <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string that matches the requested substring or characters. If the substring or character is not found, the method returns a value of -1.




## -remarks



The <a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">Find</a> method is overloaded to accept both single characters (similar to the runtime function, wcschr) and strings (similar to the runtime function, wcsstr).


#### Examples

The following code example shows the use of <b>CHString::Find</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString s( L"abcdef" );
assert( s.Find( 'c' ) == 2 );
assert( s.Find( L"de" ) == 3 );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/f3f9111d-9191-4ba5-877a-736e11d0a168">CHString::FindOneOf</a>



<a href="https://msdn.microsoft.com/941c9eb3-a5b8-42b7-bb9f-732eaf1faa24">CHString::ReverseFind</a>
 

 

