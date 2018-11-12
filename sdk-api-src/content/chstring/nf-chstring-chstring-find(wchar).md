---
UID: NF:chstring.CHString.Find(WCHAR)
title: CHString::Find(WCHAR)
author: windows-sdk-content
description: The Find method searches a string for the first match of a substring.
old-location: wmi\chstring_find_wchar_.htm
tech.root: WmiSdk
ms.assetid: f25db53e-f1a2-4b22-98de-b53ccf3952a1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "?Find@CHString@@QBEHG@Z, ?Find@CHString@@QEBAHG@Z, CHString interface [Windows Management Instrumentation],Find method, CHString.Find, CHString.Find(WCHAR), CHString::Find, CHString::Find(WCHAR), Find, Find method [Windows Management Instrumentation], Find method [Windows Management Instrumentation],CHString interface, chstring/CHString::Find, wmi.chstring_find_wchar_"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: chstring.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.Find
 - ?Find@CHString@@QBEHG@Z
 - ?Find@CHString@@QEBAHG@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::Find(WCHAR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">Find</a> method searches a string for the first match of a substring.


## -parameters




### -param ch

A single character that the method searches for.


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
 

 

