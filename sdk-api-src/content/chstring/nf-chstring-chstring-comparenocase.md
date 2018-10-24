---
UID: NF:chstring.CHString.CompareNoCase
title: CHString::CompareNoCase
author: windows-sdk-content
description: The CompareNoCase method uses the _wcsicmp function to compare a CHString string with another string.
old-location: wmi\chstring_comparenocase.htm
tech.root: WmiSdk
ms.assetid: 72ad2532-ece8-43e2-b768-7dec6a378c98
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "?CompareNoCase@CHString@@QBEHPBG@Z, ?CompareNoCase@CHString@@QEBAHPEBG@Z, CHString interface [Windows Management Instrumentation],CompareNoCase method, CHString.CompareNoCase, CHString::CompareNoCase, CompareNoCase, CompareNoCase method [Windows Management Instrumentation], CompareNoCase method [Windows Management Instrumentation],CHString interface, _hmm_chstring_comparenocase, chstring/CHString::CompareNoCase, wmi.chstring_comparenocase"
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
 - CHString.CompareNoCase
 - ?CompareNoCase@CHString@@QBEHPBG@Z
 - ?CompareNoCase@CHString@@QEBAHPEBG@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

