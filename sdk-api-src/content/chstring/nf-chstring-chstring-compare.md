---
UID: NF:chstring.CHString.Compare
title: CHString::Compare (chstring.h)
description: The Compare method uses the wcscmp function to compare this CHString string with another string.
helpviewer_keywords: ["?Compare@CHString@@QBEHPBG@Z","?Compare@CHString@@QEBAHPEBG@Z","CHString interface [Windows Management Instrumentation]","Compare method","CHString.Compare","CHString::Compare","Compare","Compare method [Windows Management Instrumentation]","Compare method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_compare","chstring/CHString::Compare","wmi.chstring_compare"]
old-location: wmi\chstring_compare.htm
tech.root: wmi
ms.assetid: 6e587dd3-b3ae-4afa-9582-b3867d2fb7ef
ms.date: 12/05/2018
ms.keywords: ?Compare@CHString@@QBEHPBG@Z, ?Compare@CHString@@QEBAHPEBG@Z, CHString interface [Windows Management Instrumentation],Compare method, CHString.Compare, CHString::Compare, Compare, Compare method [Windows Management Instrumentation], Compare method [Windows Management Instrumentation],CHString interface, _hmm_chstring_compare, chstring/CHString::Compare, wmi.chstring_compare
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHString::Compare
 - chstring/CHString::Compare
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString.Compare
 - ?Compare@CHString@@QBEHPBG@Z
 - ?Compare@CHString@@QEBAHPEBG@Z
---

# CHString::Compare


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Compare</b> method uses the wcscmp function to compare this <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string with another string.

## -parameters

### -param lpsz

The other string used for comparison.

## -returns

The <b>Compare</b> method returns the following values.

## -remarks

The <b>Compare</b> method, which performs a case-sensitive comparison of the strings, is not affected by locale.


#### Examples

The following code example shows the use of <b>CHString::Compare</b>:


```cpp
CHString s1( L"abc" );
CHString s2( L"ABC" );

assert( s1.Compare( s2 ) > 0 ); // Compare with another CHString.
assert( s1.Compare( L"abc" ) == 0 ); // Compare with LPCWSTR string.
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-collate">CHString::Collate</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-comparenocase">CHString::CompareNoCase</a>