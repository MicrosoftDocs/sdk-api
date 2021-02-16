---
UID: NF:chstrarr.CHStringArray.SetSize
title: CHStringArray::SetSize (chstrarr.h)
description: The SetSize method establishes the size of an empty or existing array.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","SetSize method","CHStringArray.SetSize","CHStringArray::SetSize","SetSize","SetSize method [Windows Management Instrumentation]","SetSize method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_setsize","chstrarr/CHStringArray::SetSize","wmi.chstringarray_setsize"]
old-location: wmi\chstringarray_setsize.htm
tech.root: wmi
ms.assetid: 9320b6b6-5253-419e-a293-3b9d030f5963
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],SetSize method, CHStringArray.SetSize, CHStringArray::SetSize, SetSize, SetSize method [Windows Management Instrumentation], SetSize method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_setsize, chstrarr/CHStringArray::SetSize, wmi.chstringarray_setsize
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
 - CHStringArray::SetSize
 - chstrarr/CHStringArray::SetSize
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
 - CHStringArray.SetSize
---

# CHStringArray::SetSize


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetSize</b> method establishes the size of an empty or existing array.

## -parameters

### -param nNewSize

The new array size (number of elements). The value must be greater than or equal to 0 (zero).

### -param nGrowBy

The minimum number of element slots to allocate if a size increase is necessary.

## -returns

This method does not return a value.

## -remarks

The <b>SetSize</b> method allocates memory if necessary. If the new size is smaller than the old size, then the array is truncated, and all unused memory is released. For efficiency, call <b>SetSize</b> to set the size of the array before using it. This prevents the need to reallocate and copy the array each time an item is added.

The <i>nGrowBy</i> parameter affects internal memory allocation while the array is growing. Its use never affects the array size as reported by <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getsize">GetSize</a> and <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">GetUpperBound</a>.


#### Examples

See the example for <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getdata">CHStringArray::GetData</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getdata">CHStringArray::GetData</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getsize">CHStringArray::GetSize</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">CHStringArray::GetUpperBound</a>