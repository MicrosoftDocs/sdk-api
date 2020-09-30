---
UID: NF:chstring.CHString.Find(LPCWSTR)
title: CHString::Find(LPCWSTR) (chstring.h)
description: The Find method searches a string for the first match of a substring.
helpviewer_keywords: ["?Find@CHString@@QBEHPBG@Z","?Find@CHString@@QEBAHPEBG@Z","CHString interface [Windows Management Instrumentation]","Find method","CHString.Find","CHString.Find(LPCWSTR)","CHString::Find","CHString::Find(LPCWSTR)","Find","Find method [Windows Management Instrumentation]","Find method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_find","chstring/CHString::Find","wmi.chstring_find_lpcwstr_"]
old-location: wmi\chstring_find_lpcwstr_.htm
tech.root: wmi
ms.assetid: d2a8998c-e0e3-47d0-9539-9ae1d1fba5c8
ms.date: 12/05/2018
ms.keywords: ?Find@CHString@@QBEHPBG@Z, ?Find@CHString@@QEBAHPEBG@Z, CHString interface [Windows Management Instrumentation],Find method, CHString.Find, CHString.Find(LPCWSTR), CHString::Find, CHString::Find(LPCWSTR), Find, Find method [Windows Management Instrumentation], Find method [Windows Management Instrumentation],CHString interface, _hmm_chstring_find, chstring/CHString::Find, wmi.chstring_find_lpcwstr_
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
 - CHString::Find
 - chstring/CHString::Find
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
 - CHString.Find
 - ?Find@CHString@@QBEHPBG@Z
 - ?Find@CHString@@QEBAHPEBG@Z
---

# CHString::Find(LPCWSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/api/chstring/nf-chstring-chstring-find(wchar)">Find</a> method searches a string for the first match of a substring.

## -parameters

### -param lpszSub

A substring that the method searches for.

## -returns

If the <a href="/windows/desktop/api/chstring/nf-chstring-chstring-find(wchar)">Find</a> method is successful, it returns the zero-based index of the first character in this <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string that matches the requested substring or characters. If the substring or character is not found, the method returns a value of -1.

## -remarks

The <a href="/windows/desktop/api/chstring/nf-chstring-chstring-find(wchar)">Find</a> method is overloaded to accept both single characters (similar to the runtime function, wcschr) and strings (similar to the runtime function, wcsstr).


#### Examples

The following code example shows the use of <b>CHString::Find</b>.


```cpp
CHString s( L"abcdef" );
assert( s.Find( 'c' ) == 2 );
assert( s.Find( L"de" ) == 3 );
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-findoneof">CHString::FindOneOf</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-reversefind">CHString::ReverseFind</a>