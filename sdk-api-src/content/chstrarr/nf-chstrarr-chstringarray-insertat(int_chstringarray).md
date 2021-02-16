---
UID: NF:chstrarr.CHStringArray.InsertAt(int,CHStringArray)
title: CHStringArray::InsertAt(int,CHStringArray) (chstrarr.h)
description: The InsertAt method inserts all of the elements of another CHStringArray array at the index specified by nStartIndex.
helpviewer_keywords: ["CHStringArray.InsertAt","CHStringArray.InsertAt(int","CHStringArray)","CHStringArray::InsertAt","CHStringArray::InsertAt methods [Windows Management Instrumentation]","CHStringArray::InsertAt(int","CHStringArray)","InsertAt","chstrarr/CHStringArray::InsertAt","wmi.insertat_method_in_class_chstringarray"]
old-location: wmi\chstringarray_insertat_int__chstringarray__.htm
tech.root: wmi
ms.assetid: 4aab5eb2-0b6d-4ffc-b627-a35c0696c7cc
ms.date: 12/05/2018
ms.keywords: CHStringArray.InsertAt, CHStringArray.InsertAt(int,CHStringArray), CHStringArray::InsertAt, CHStringArray::InsertAt methods [Windows Management Instrumentation], CHStringArray::InsertAt(int,CHStringArray), InsertAt, chstrarr/CHStringArray::InsertAt, wmi.insertat_method_in_class_chstringarray
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
 - CHStringArray::InsertAt
 - chstrarr/CHStringArray::InsertAt
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
 - CHStringArray.InsertAt(int, CHStringArray*)
---

# CHStringArray::InsertAt(int,CHStringArray)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>InsertAt</b> method inserts  all of the elements of another <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> array at the index specified by <i>nStartIndex</i>.

## -parameters

### -param nStartIndex

Type: <b>int</b>

An integer index that can be greater than the value returned by <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.

### -param pNewArray

Type: <b>CHStringArray*</b>

Pointer to another <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> that contains the elements to be inserted into this array.

## -returns

This method does not return a value.

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-removeat">CHStringArray::RemoveAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setat(int_lpcwstr)">CHStringArray::SetAt</a>