---
UID: NF:chstring.CHString.Compare
title: CHString::Compare
author: windows-sdk-content
description: The Compare method uses the wcscmp function to compare this CHString string with another string.
old-location: wmi\chstring_compare.htm
tech.root: WmiSdk
ms.assetid: 6e587dd3-b3ae-4afa-9582-b3867d2fb7ef
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "?Compare@CHString@@QBEHPBG@Z, ?Compare@CHString@@QEBAHPEBG@Z, CHString interface [Windows Management Instrumentation],Compare method, CHString.Compare, CHString::Compare, Compare, Compare method [Windows Management Instrumentation], Compare method [Windows Management Instrumentation],CHString interface, _hmm_chstring_compare, chstring/CHString::Compare, wmi.chstring_compare"
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
 - CHString.Compare
 - ?Compare@CHString@@QBEHPBG@Z
 - ?Compare@CHString@@QEBAHPEBG@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::Compare


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Compare</b> method uses the wcscmp function to compare this <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string with another string.


## -parameters




### -param lpsz

The other string used for comparison.


## -returns



The <b>Compare</b> method returns the following values.




## -remarks



The <b>Compare</b> method, which performs a case-sensitive comparison of the strings, is not affected by locale.


#### Examples

The following code example shows the use of <b>CHString::Compare</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString s1( L"abc" );
CHString s2( L"ABC" );

assert( s1.Compare( s2 ) &gt; 0 ); // Compare with another CHString.
assert( s1.Compare( L"abc" ) == 0 ); // Compare with LPCWSTR string.</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/b6c88b83-a369-4cb2-9297-df9c5911d08f">CHString::Collate</a>



<a href="https://msdn.microsoft.com/72ad2532-ece8-43e2-b768-7dec6a378c98">CHString::CompareNoCase</a>
 

 

