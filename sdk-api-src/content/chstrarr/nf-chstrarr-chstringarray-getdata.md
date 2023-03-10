---
UID: NF:chstrarr.CHStringArray.GetData
title: CHStringArray::GetData (chstrarr.h)
description: The GetData method gains direct access to the elements in the array.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","GetData method","CHStringArray.GetData","CHStringArray::GetData","GetData","GetData method [Windows Management Instrumentation]","GetData method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_getdata","chstrarr/CHStringArray::GetData","wmi.chstringarray_getdata"]
old-location: wmi\chstringarray_getdata.htm
tech.root: wmi
ms.assetid: b59a0c42-e753-43ff-bf39-279f0a8b9d2b
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],GetData method, CHStringArray.GetData, CHStringArray::GetData, GetData, GetData method [Windows Management Instrumentation], GetData method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getdata, chstrarr/CHStringArray::GetData, wmi.chstringarray_getdata
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
 - CHStringArray::GetData
 - chstrarr/CHStringArray::GetData
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
 - CHStringArray.GetData
---

# CHStringArray::GetData


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetData</b> method gains direct access to the elements in the array.



## -returns

If the <b>GetData</b> method is successful, it returns a pointer to the array of <a href="/windows/desktop/WmiSdk/chstring">CHString</a> pointers.

## -remarks

If no elements are available,  <b>GetData</b> returns a <b>NULL</b> value.

Although direct access to the elements of an array can help you work more quickly, use caution when calling <b>GetData</b>. Any errors you make directly affect the elements of your array.

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-elementat(int)">CHStringArray::ElementAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-freeextra">CHStringArray::FreeExtra</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getat(int)">CHStringArray::GetAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setat(int_lpcwstr)">CHStringArray::SetAt</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setsize">CHStringArray::SetSize</a>
