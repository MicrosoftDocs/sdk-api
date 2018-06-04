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

# CHString::GetAt(int)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method returns a single character specified by an index number.


## -parameters




### -param nIndex

Zero-based index of the character in the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to zero (0), and less than the value returned by <a href="https://msdn.microsoft.com/b898f9d1-b9a2-4c7b-a7c0-1b6b51ae565f">GetLength</a>. The debug version of the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

## -returns



Returns a <b>WCHAR</b> that contains the character at the specified place in the string.




## -remarks



The overloaded subscript (<a href="https://msdn.microsoft.com/9a0ba1f3-e862-4210-86a4-55a573e8bb4b">[]</a>) operator is a convenient alternative for <b>GetAt</b>.


#### Examples

The following code example shows the use of <b>CHString::GetAt</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString s( L"abcdef" );
assert( s.GetAt(2) == 'c' );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/b898f9d1-b9a2-4c7b-a7c0-1b6b51ae565f">CHString::GetLength</a>



<a href="https://msdn.microsoft.com/9a0ba1f3-e862-4210-86a4-55a573e8bb4b">CHString::operator[]</a>
 

 

