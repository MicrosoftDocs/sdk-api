---
UID: NF:chstring.CHString.Collate
title: CHString::Collate
author: windows-driver-content
description: The Collate method uses the wcscoll function to compare a CHString string with another string.
old-location: wmi\chstring_collate.htm
old-project: WmiSdk
ms.assetid: b6c88b83-a369-4cb2-9297-df9c5911d08f
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CHString interface [Windows Management Instrumentation],Collate method, CHString.Collate, CHString::Collate, Collate, Collate method [Windows Management Instrumentation], Collate method [Windows Management Instrumentation],CHString interface, _hmm_chstring_collate, chstring/CHString::Collate, wmi.chstring_collate
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
req.typenames: CF_SYNC_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.Collate
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::Collate


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Collate</b> method uses the wcscoll function to compare a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string with another string.


## -parameters




### -param lpsz

The other string used for comparison.


## -returns



The <b>Collate</b> method returns the following values.




## -remarks



The <b>Collate</b> method performs a case-sensitive comparison of the strings according to the code page currently in use.


#### Examples

The following code example shows how to use <b>CHString::Collate</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString str1 = L"co-op";
CHString str2 = L"con";

int n;

// collation uses language rules, such as ignoring dashes
n = str1.Collate(str2);
assert(n &gt; 0);

// comparison is a strict ASCII comparison with no language rules
n = str1.Compare(str2);
assert(n &lt; 0);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/6e587dd3-b3ae-4afa-9582-b3867d2fb7ef">CHString::Compare</a>



<a href="https://msdn.microsoft.com/72ad2532-ece8-43e2-b768-7dec6a378c98">CHString::CompareNoCase</a>
 

 

