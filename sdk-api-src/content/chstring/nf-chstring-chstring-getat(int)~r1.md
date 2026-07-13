---
UID: NF:chstring.CHString.GetAt(int)~r1
title: CHString::GetAt (chstring.h)
description: The CHString::GetAt (chstring.h) method returns a single character specified by an index number.
helpviewer_keywords: ["CHString interface [Windows Management Instrumentation]","GetAt method","CHString.GetAt","CHString::GetAt","GetAt","GetAt method [Windows Management Instrumentation]","GetAt method [Windows Management Instrumentation]","CHString interface","_hmm_chstring_getat","chstring/CHString::GetAt","wmi.chstring_getat"]
old-location: wmi\chstring_getat.htm
tech.root: wmi
ms.assetid: ed038b41-211c-4483-99cd-0bc43b241761
ms.date: 08/10/2022
ms.keywords: CHString interface [Windows Management Instrumentation],GetAt method, CHString.GetAt, CHString::GetAt, GetAt, GetAt method [Windows Management Instrumentation], GetAt method [Windows Management Instrumentation],CHString interface, _hmm_chstring_getat, chstring/CHString::GetAt, wmi.chstring_getat
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
 - CHString::GetAt
 - chstring/CHString::GetAt
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
 - CHString.GetAt
---

# CHString::GetAt


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method returns a single character specified by an index number.

## -parameters

### -param nIndex

Zero-based index of the character in the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to zero (0), and less than the value returned by <a href="/windows/desktop/api/chstring/nf-chstring-chstring-getlength">GetLength</a>. The debug version of the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

## -returns

Returns a <b>WCHAR</b> that contains the character at the specified place in the string.

## -remarks

The overloaded subscript (<a href="/previous-versions/windows/desktop/legacy/aa386162(v=vs.85)">[]</a>) operator is a convenient alternative for <b>GetAt</b>.


#### Examples

The following code example shows the use of <b>CHString::GetAt</b>:


```cpp
CHString s( L"abcdef" );
assert( s.GetAt(2) == 'c' );
```

## -see-also

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>



<a href="/windows/desktop/api/chstring/nf-chstring-chstring-getlength">CHString::GetLength</a>



<a href="/previous-versions/windows/desktop/legacy/aa386162(v=vs.85)">CHString::operator[]</a>