---
UID: NF:chstring.CHString.Mid(int,int)
title: CHString::Mid(int,int)
author: windows-sdk-content
description: The Mid method extracts a substring of length nCount characters from a CHString string, starting at position nFirst (zero-based). The method returns a copy of the extracted substring.
old-location: wmi\chstring_mid_int_int_.htm
tech.root: WmiSdk
ms.assetid: f79f7b70-0587-4d5d-8a18-c61bd3c69212
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "?Mid@CHString@@QBE?AV1@HH@Z, ?Mid@CHString@@QEBA?AV1@HH@Z, CHString interface [Windows Management Instrumentation],Mid method, CHString.Mid, CHString.Mid(int,int), CHString::Mid, CHString::Mid(int,int), Mid, Mid method [Windows Management Instrumentation], Mid method [Windows Management Instrumentation],CHString interface, chstring/CHString::Mid, wmi.chstring_mid_int_int_"
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
 - CHString.Mid
 - ?Mid@CHString@@QBE?AV1@HH@Z
 - ?Mid@CHString@@QEBA?AV1@HH@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- chstring.h
: 
- CHString.Mid
: 
---

# CHString::Mid(int,int)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/2036813b-f991-4ca3-95d3-8bbe858aae09">Mid</a> method extracts a substring of length <i>nCount</i> characters from a 
<b>CHString</b> string, starting at position <i>nFirst</i> (zero-based). The method returns a copy of the extracted substring.


## -parameters




### -param nFirst

The zero-based index of the first character in this <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string that is be included in the extracted substring.


### -param nCount

The number of characters to extract form this <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string. If this parameter is not supplied, then the remainder of the string is extracted.


## -returns



Returns a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> object that contains a copy of the specified range of characters. The returned <b>CHString</b> object may be empty.




## -remarks



The <a href="https://msdn.microsoft.com/2036813b-f991-4ca3-95d3-8bbe858aae09">Mid</a> method is similar to the Basic <b>MID$</b> function except in the Basic <b>MID$</b> function, indexes are zero-based.


#### Examples

The following code example shows the use of <b>CHString::Mid</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString s( L"abcdef" );
assert( s.Mid( 2, 3 ) == L"cde" );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/52219bbb-0a88-47b3-ac6c-ba54d15e8157">CHString::Left</a>



<a href="https://msdn.microsoft.com/eccf928f-75ac-4442-90f9-0e0578c5798f">CHString::Right</a>
 

 

