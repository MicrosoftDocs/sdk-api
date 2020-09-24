---
UID: NF:chstrarr.CHStringArray.RemoveAt
title: CHStringArray::RemoveAt (chstrarr.h)
description: The RemoveAt method removes one or more elements starting at a specified index in an array.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","RemoveAt method","CHStringArray.RemoveAt","CHStringArray::RemoveAt","RemoveAt","RemoveAt method [Windows Management Instrumentation]","RemoveAt method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_removeat","chstrarr/CHStringArray::RemoveAt","wmi.chstringarray_removeat"]
old-location: wmi\chstringarray_removeat.htm
tech.root: wmi
ms.assetid: b7555074-4f9a-46be-b321-f16e00663c32
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],RemoveAt method, CHStringArray.RemoveAt, CHStringArray::RemoveAt, RemoveAt, RemoveAt method [Windows Management Instrumentation], RemoveAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_removeat, chstrarr/CHStringArray::RemoveAt, wmi.chstringarray_removeat
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
 - CHStringArray::RemoveAt
 - chstrarr/CHStringArray::RemoveAt
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
 - CHStringArray.RemoveAt
---

# CHStringArray::RemoveAt


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>RemoveAt</b> method removes one or more elements starting at a specified index in an array.

## -parameters

### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.

### -param nCount

The number of elements to remove. The default is 1 (one).

## -remarks

In the process of removing elements,  <b>RemoveAt</b> shifts down all the elements located above the elements that are removed. This method decrements the upper bound of the array but does not free memory.


#### Examples

The following code example shows the use of <b>CHStringArray::RemoveAt</b>.


```cpp
CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1
array.RemoveAt( 0 );  // Element 1 moves to 0.
assert ( array[0] == L"String 2" );
```


The results from this program are as follows.


```cpp
[0] = String 2
```

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getat(int)">CHStringArray::GetAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)">CHStringArray::InsertAt</a>