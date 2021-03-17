---
UID: NF:chstring.CHString.SpanIncluding
title: CHString::SpanIncluding (chstring.h)
description: The SpanIncluding method extracts characters of a string that are identified by lpszCharSet.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","SpanIncluding method","CHString.SpanIncluding","CHString::SpanIncluding","SpanIncluding","SpanIncluding method [Windows Management Instrumentation]","SpanIncluding method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_spanincluding","chstring/CHString::SpanIncluding","wmi.chstring_spanincluding"]
old-location: wmi\chstring_spanincluding.htm
tech.root: wmi
ms.assetid: d99ce931-c6ec-4f1c-b4ab-144dc930f990
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],SpanIncluding method, CHString.SpanIncluding, CHString::SpanIncluding, SpanIncluding, SpanIncluding method [Windows Management Instrumentation], SpanIncluding method [Windows Management Instrumentation],CHString interface, _hmm_chstring_spanincluding, chstring/CHString::SpanIncluding, wmi.chstring_spanincluding
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
 - CHString::SpanIncluding
 - chstring/CHString::SpanIncluding
dev_langs:
 - c++
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
---

# CHString::SpanIncluding


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
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


```cpp
CHString str( L"cabbage" );
CHString res = str.SpanIncluding( L"abc" );

assert( res == L"cabba" );
res = str.SpanIncluding( L"xyz" );
assert( res.IsEmpty( ) );
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-isempty">CHString::IsEmpty</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-spanexcluding">CHString::SpanExcluding</a>