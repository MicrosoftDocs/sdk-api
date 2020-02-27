---
UID: NF:chstring.CHString.CompareNoCase
title: CHString::CompareNoCase (chstring.h)
description: The CompareNoCase method uses the _wcsicmp function to compare a CHString string with another string.
old-location: wmi\chstring_comparenocase.htm
tech.root: WmiSdk
ms.assetid: 72ad2532-ece8-43e2-b768-7dec6a378c98
ms.date: 12/05/2018
ms.keywords: ?CompareNoCase@CHString@@QBEHPBG@Z, ?CompareNoCase@CHString@@QEBAHPEBG@Z, CHString interface [Windows Management Instrumentation],CompareNoCase method, CHString.CompareNoCase, CHString::CompareNoCase, CompareNoCase, CompareNoCase method [Windows Management Instrumentation], CompareNoCase method [Windows Management Instrumentation],CHString interface, _hmm_chstring_comparenocase, chstring/CHString::CompareNoCase, wmi.chstring_comparenocase
f1_keywords:
- chstring/CHString.CompareNoCase
dev_langs:
- c++
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
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CHString.CompareNoCase
- ?CompareNoCase@CHString@@QBEHPBG@Z
- ?CompareNoCase@CHString@@QEBAHPEBG@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHString::CompareNoCase


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>CompareNoCase</b> method uses the _wcsicmp function to compare a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> string with another string.


## -parameters




### -param lpsz

The other string used for comparison.


## -returns



The <b>CompareNoCase</b> method returns the following values.




## -remarks



The <b>CompareNoCase</b> method, which performs a case-insensitive comparison of the strings, is not affected by locale.


#### Examples

The following code  example shows the use of <b>CHstring::CompareNoCase</b>:


```cpp
CHString s1( L"abc" );
CHString s2( L"ABD" );

// Compare with a CHString.
assert( s1.CompareNoCase( s2 ) == 0 );
// Compare with LPCWSTR string.
assert( s1.CompareNoCase( L"ABE" ) < 0 );
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-collate">CHString::Collate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-compare">CHString::Compare</a>
 

 

