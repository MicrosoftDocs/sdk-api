---
UID: NF:chstring.CHString.Find(LPCWSTR)
title: CHString::Find(LPCWSTR) (chstring.h)
author: windows-sdk-content
description: The Find method searches a string for the first match of a substring.
old-location: wmi\chstring_find_lpcwstr_.htm
tech.root: WmiSdk
ms.assetid: d2a8998c-e0e3-47d0-9539-9ae1d1fba5c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "?Find@CHString@@QBEHPBG@Z, ?Find@CHString@@QEBAHPEBG@Z, CHString interface [Windows Management Instrumentation],Find method, CHString.Find, CHString.Find(LPCWSTR), CHString::Find, CHString::Find(LPCWSTR), Find, Find method [Windows Management Instrumentation], Find method [Windows Management Instrumentation],CHString interface, _hmm_chstring_find, chstring/CHString::Find, wmi.chstring_find_lpcwstr_"
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
 - ?Find@CHString@@QBEHPBG@Z
 - ?Find@CHString@@QEBAHPEBG@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```cpp
CHString s( L"abcdef" );
assert( s.Find( 'c' ) == 2 );
assert( s.Find( L"de" ) == 3 );
```





## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/f3f9111d-9191-4ba5-877a-736e11d0a168">CHString::FindOneOf</a>



<a href="https://msdn.microsoft.com/941c9eb3-a5b8-42b7-bb9f-732eaf1faa24">CHString::ReverseFind</a>
 

 

