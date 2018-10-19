---
UID: NF:chstring.CHString.SpanIncluding
title: CHString::SpanIncluding
author: windows-sdk-content
description: The SpanIncluding method extracts characters of a string that are identified by lpszCharSet.
old-location: wmi\chstring_spanincluding.htm
tech.root: WmiSdk
ms.assetid: d99ce931-c6ec-4f1c-b4ab-144dc930f990
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CHString interface [Windows Management Instrumentation],SpanIncluding method, CHString.SpanIncluding, CHString::SpanIncluding, SpanIncluding, SpanIncluding method [Windows Management Instrumentation], SpanIncluding method [Windows Management Instrumentation],CHString interface, _hmm_chstring_spanincluding, chstring/CHString::SpanIncluding, wmi.chstring_spanincluding
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
 - CHString.SpanIncluding
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CHString::SpanIncluding


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SpanIncluding</b> method extracts characters of a string that are identified by <i>lpszCharSet</i>.


## -parameters




### -param lpszCharSet

A string interpreted as a set of characters.


## -returns



The <b>SpanIncluding</b> method returns a substring that contains characters in the string that are in <i>lpszCharSet</i>.

If the first character in the string is not in the specified set, the method returns an empty substring.




## -remarks



The <b>SpanIncluding</b> method starts with the first character of the string and stops when a character is found in the string but not in <i>lpszCharSet</i>.


#### Examples

The following code example shows the use of <b>CHString::SpanIncluding</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString str( L"cabbage" );
CHString res = str.SpanIncluding( L"abc" );

assert( res == L"cabba" );
res = str.SpanIncluding( L"xyz" );
assert( res.IsEmpty( ) );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/06af1063-1e5a-4a09-a0d7-b5567b9efcff">CHString::IsEmpty</a>



<a href="https://msdn.microsoft.com/5ddadf16-0177-4f96-a5ca-e1b8891473e6">CHString::SpanExcluding</a>
 

 

