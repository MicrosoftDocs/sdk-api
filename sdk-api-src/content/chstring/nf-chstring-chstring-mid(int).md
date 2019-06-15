---
UID: NF:chstring.CHString.Mid(int)
title: CHString::Mid(int) (chstring.h)
author: windows-sdk-content
description: The Mid method extracts a substring of length nCount characters from a CHString string, starting at position nFirst (zero-based). The method returns a copy of the extracted substring.
old-location: wmi\chstring_mid_int_.htm
tech.root: WmiSdk
ms.assetid: dfc52075-2323-438e-9fe9-7ca3f2de2e35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],Mid method, CHString.Mid, CHString.Mid(int), CHString::Mid, CHString::Mid(int), Mid, Mid method [Windows Management Instrumentation], Mid method [Windows Management Instrumentation],CHString interface, chstring/CHString::Mid, wmi.chstring_mid_int_
ms.topic: method
f1_keywords: ["chstring/CHString.Mid"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHString::Mid(int)


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-mid">Mid</a> method extracts a substring of length <i>nCount</i> characters from a 
<b>CHString</b> string, starting at position <i>nFirst</i> (zero-based). The method returns a copy of the extracted substring.


## -parameters




### -param nFirst

The zero-based index of the first character in this <b>CHString</b> string that is be included in the extracted substring.


## -returns



Returns a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> object that contains a copy of the specified range of characters. The returned <b>CHString</b> object may be empty.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-mid">Mid</a> method is similar to the Basic <b>MID$</b> function except in the Basic <b>MID$</b> function, indexes are zero-based.


#### Examples

The following code example shows the use of <b>CHString::Mid</b>.


```cpp
CHString s( L"abcdef" );
assert( s.Mid( 2, 3 ) == L"cde" );
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-left">CHString::Left</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-right">CHString::Right</a>
 

 

