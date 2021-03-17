---
UID: NF:chstring.CHString.Collate
title: CHString::Collate (chstring.h)
description: The Collate method uses the wcscoll function to compare a CHString string with another string.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","Collate method","CHString.Collate","CHString::Collate","Collate","Collate method [Windows Management Instrumentation]","Collate method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_collate","chstring/CHString::Collate","wmi.chstring_collate"]
old-location: wmi\chstring_collate.htm
tech.root: wmi
ms.assetid: b6c88b83-a369-4cb2-9297-df9c5911d08f
ms.date: 12/05/2018
ms.keywords: CHString interface [Windows Management Instrumentation],Collate method, CHString.Collate, CHString::Collate, Collate, Collate method [Windows Management Instrumentation], Collate method [Windows Management Instrumentation],CHString interface, _hmm_chstring_collate, chstring/CHString::Collate, wmi.chstring_collate
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
 - CHString::Collate
 - chstring/CHString::Collate
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
 - CHString.Collate
---

# CHString::Collate


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Collate</b> method uses the wcscoll function to compare a <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string with another string.

## -parameters

### -param lpsz

The other string used for comparison.

## -returns

The <b>Collate</b> method returns the following values.

## -remarks

The <b>Collate</b> method performs a case-sensitive comparison of the strings according to the code page currently in use.


#### Examples

The following code example shows how to use <b>CHString::Collate</b>:


```cpp
CHString str1 = L"co-op";
CHString str2 = L"con";

int n;

// collation uses language rules, such as ignoring dashes
n = str1.Collate(str2);
assert(n > 0);

// comparison is a strict ASCII comparison with no language rules
n = str1.Compare(str2);
assert(n < 0);
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-compare">CHString::Compare</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-comparenocase">CHString::CompareNoCase</a>