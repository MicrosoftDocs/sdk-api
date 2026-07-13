---
UID: NF:chstrarr.CHStringArray.GetUpperBound
title: CHStringArray::GetUpperBound (chstrarr.h)
description: The GetUpperBound method gets the current upper bound of an array. Because array indexes are zero-based, this function returns a value that is one less than GetSize.
helpviewer_keywords: ["?GetUpperBound@CHStringArray@@QBEHXZ","?GetUpperBound@CHStringArray@@QEBAHXZ","CHStringArray interface [Windows Management Instrumentation]","GetUpperBound method","CHStringArray.GetUpperBound","CHStringArray::GetUpperBound","GetUpperBound","GetUpperBound method [Windows Management Instrumentation]","GetUpperBound method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_getupperbound","chstrarr/CHStringArray::GetUpperBound","wmi.chstringarray_getupperbound"]
old-location: wmi\chstringarray_getupperbound.htm
tech.root: wmi
ms.assetid: 77c200f9-c63b-4842-881f-5c077e4618b8
ms.date: 12/05/2018
ms.keywords: ?GetUpperBound@CHStringArray@@QBEHXZ, ?GetUpperBound@CHStringArray@@QEBAHXZ, CHStringArray interface [Windows Management Instrumentation],GetUpperBound method, CHStringArray.GetUpperBound, CHStringArray::GetUpperBound, GetUpperBound, GetUpperBound method [Windows Management Instrumentation], GetUpperBound method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getupperbound, chstrarr/CHStringArray::GetUpperBound, wmi.chstringarray_getupperbound
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
 - CHStringArray::GetUpperBound
 - chstrarr/CHStringArray::GetUpperBound
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
 - CHStringArray.GetUpperBound
 - ?GetUpperBound@CHStringArray@@QBEHXZ
 - ?GetUpperBound@CHStringArray@@QEBAHXZ
---

# CHStringArray::GetUpperBound


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetUpperBound</b> method gets the current upper bound of an array. Because array indexes are zero-based, this function returns a value that is one less than <a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getsize">GetSize</a>.



## -returns

If the <b>GetUpperBound</b> method is successful, it returns the upper bounds of this array. A value of -1 indicates that the array contains no elements.

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getsize">CHStringArray::GetSize</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setsize">CHStringArray::SetSize</a>
