---
UID: NF:chstrarr.CHStringArray.GetSize
title: CHStringArray::GetSize (chstrarr.h)
description: The GetSize method gets the size of the array. Because indexes are zero-based, the size is one greater than the largest index.
helpviewer_keywords: ["?GetSize@CHStringArray@@QEBAHXZ","CHStringArray interface [Windows Management Instrumentation]","GetSize method","CHStringArray.GetSize","CHStringArray::GetSize","GetSize","GetSize method [Windows Management Instrumentation]","GetSize method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_getsize","chstrarr/CHStringArray::GetSize","wmi.chstringarray_getsize"]
old-location: wmi\chstringarray_getsize.htm
tech.root: wmi
ms.assetid: 5db50c38-a9c7-4711-925e-291cebf2b6f1
ms.date: 12/05/2018
ms.keywords: ?GetSize@CHStringArray@@QEBAHXZ, CHStringArray interface [Windows Management Instrumentation],GetSize method, CHStringArray.GetSize, CHStringArray::GetSize, GetSize, GetSize method [Windows Management Instrumentation], GetSize method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_getsize, chstrarr/CHStringArray::GetSize, wmi.chstringarray_getsize
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
 - CHStringArray::GetSize
 - chstrarr/CHStringArray::GetSize
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
 - CHStringArray.GetSize
 - ?GetSize@CHStringArray@@QEBAHXZ
---

# CHStringArray::GetSize


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetSize</b> method gets the size of the array. Because indexes are zero-based, the size is one greater than the largest index.



## -returns

If the <b>GetSize</b> method is successful, it returns the number of elements in the array.

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-add">CHStringArray::Add</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-getupperbound">CHStringArray::GetUpperBound</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setsize">CHStringArray::SetSize</a>
