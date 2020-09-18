---
UID: NF:chstrarr.CHStringArray.GetAt(int)
title: CHStringArray::GetAt(int) (chstrarr.h)
description: Gets the array element at the specified index.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","GetAt method","CHStringArray.GetAt","CHStringArray.GetAt(int)","CHStringArray::GetAt","CHStringArray::GetAt(int)","GetAt","GetAt method [Windows Management Instrumentation]","GetAt method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_getat","chstrarr/CHStringArray::GetAt","wmi.chstringarray_getat"]
old-location: wmi\chstringarray_getat.htm
tech.root: wmi
ms.assetid: a950bc1e-1c13-4880-aee7-9a4606979993
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],GetAt method, CHStringArray.GetAt, CHStringArray.GetAt(int), CHStringArray::GetAt, CHStringArray::GetAt(int), GetAt, GetAt method [Windows Management Instrumentation], GetAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getat, chstrarr/CHStringArray::GetAt, wmi.chstringarray_getat
req.header: chstrarr.h
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
 - CHStringArray::GetAt
 - chstrarr/CHStringArray::GetAt
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
 - CHStringArray.GetAt
---

# CHStringArray::GetAt(int)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method gets the array element at the specified index.

## -parameters

### -param nIndex

An integer index that is greater than or equal to zero (0), and less than or equal to the value returned by <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to 0. The debug version of the <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

## -returns

If the <b>GetAt</b> method is successful, it returns the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> pointer element currently at this index.

## -remarks

Passing a negative value or a value greater than the value returned by <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a> results in a failed assertion for debug builds.


#### Examples

The following code example shows the use of <b>CHStringArray::GetAt</b>.


```cpp
CHStringArray array;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
assert( array.GetAt( 0 ) == "String 1" );
```

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-elementat(int)">CHStringArray::ElementAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getdata">CHStringArray::GetData</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setat(int_lpcwstr)">CHStringArray::SetAt</a>



<a href="/windows/desktop/WmiSdk/chstringarray--operator-brackets">CHStringArray::operator []</a>