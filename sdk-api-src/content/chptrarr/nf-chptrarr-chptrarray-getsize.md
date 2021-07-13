---
UID: NF:chptrarr.CHPtrArray.GetSize
title: CHPtrArray::GetSize (chptrarr.h)
description: The GetSize function obtains the pointer array size. Because indexes are zero-based, the size is one greater than the largest index.
helpviewer_keywords: ["?GetSize@CHPtrArray@@QBEHXZ","CHPtrArray interface [Windows Management Instrumentation]","GetSize method","CHPtrArray.GetSize","CHPtrArray::GetSize","GetSize","GetSize method [Windows Management Instrumentation]","GetSize method [Windows Management Instrumentation]","CHPtrArray interface","chptrarr/CHPtrArray::GetSize","wmi.chptrarray_getsize"]
old-location: wmi\chptrarray_getsize.htm
tech.root: wmi
ms.assetid: 9b9bcd3f-06d9-47f1-aecb-1c611c9866bd
ms.date: 12/05/2018
ms.keywords: ?GetSize@CHPtrArray@@QBEHXZ, CHPtrArray interface [Windows Management Instrumentation],GetSize method, CHPtrArray.GetSize, CHPtrArray::GetSize, GetSize, GetSize method [Windows Management Instrumentation], GetSize method [Windows Management Instrumentation],CHPtrArray interface, chptrarr/CHPtrArray::GetSize, wmi.chptrarray_getsize
req.header: chptrarr.h
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
 - CHPtrArray::GetSize
 - chptrarr/CHPtrArray::GetSize
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
 - CHPtrArray.GetSize
 - ?GetSize@CHPtrArray@@QBEHXZ
---

# CHPtrArray::GetSize


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chptrarr/nl-chptrarr-chptrarray">CHPtrArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetSize</b> function obtains the pointer array size. Because indexes are zero-based, the size is one greater than the largest index.



## -returns

If the <b>GetSize</b> method is successful, it returns the number of elements in the array.

## -see-also

<a href="/windows/desktop/api/chptrarr/nl-chptrarr-chptrarray">CHPtrArray</a>



<a href="/windows/desktop/WmiSdk/provider-framework-utility-classes">Provider Framework Utility Classes</a>
