---
UID: NF:chstrarr.CHStringArray.SetAt(int,LPCWSTR)~r1
title: CHStringArray::SetAt (chstrarr.h)
description: The CHStringArray::SetAt (chstrarr.h) method sets the array element at the specified index.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","SetAt method","CHStringArray.SetAt","CHStringArray::SetAt","SetAt","SetAt method [Windows Management Instrumentation]","SetAt method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_setat","chstrarr/CHStringArray::SetAt","wmi.chstringarray_setat"]
old-location: wmi\chstringarray_setat.htm
tech.root: wmi
ms.assetid: 709bed59-c154-4103-9d38-398945657ec6
ms.date: 08/10/2022
ms.keywords: CHStringArray interface [Windows Management Instrumentation],SetAt method, CHStringArray.SetAt, CHStringArray::SetAt, SetAt, SetAt method [Windows Management Instrumentation], SetAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_setat, chstrarr/CHStringArray::SetAt, wmi.chstringarray_setat
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
 - CHStringArray::SetAt
 - chstrarr/CHStringArray::SetAt
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
 - CHStringArray.SetAt
---

# CHStringArray::SetAt


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetAt</b> method sets the array element at the specified index.

## -parameters

### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.

### -param newElement

The object pointer that is inserted in this array. A <b>NULL</b> value is allowed.

## -remarks

The <b>SetAt</b> method does not cause the array to increase. Use <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setatgrow">SetAtGrow</a> if you want the array to increase automatically.

You must ensure that your index value represents a valid position in the array.


#### Examples

The following code example shows the use of <b>CHStringArray::SetAt</b>.


```cpp
CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1
array.SetAt( 0, L"String 3" );  // Replace element 0.
assert( array[0] == "String 3" );
```


The following  example results in a <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> with two elements.


```cpp
    [0] = String 3
    [1] = String 2
```

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-elementat(int)">CHStringArray::ElementAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getat(int)">CHStringArray::GetAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getdata">CHStringArray::GetData</a>



<a href="/windows/desktop/WmiSdk/chstringarray--operator-brackets">CHStringArray::operator []</a>