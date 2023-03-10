---
UID: NF:chptrarr.CHPtrArray.GetAt
title: CHPtrArray::GetAt (chptrarr.h)
description: The GetAt method accesses an element in a CHPtrArray array.
helpviewer_keywords: ["?GetAt@CHPtrArray@@QBEPAXH@Z","CHPtrArray interface [Windows Management Instrumentation]","GetAt method","CHPtrArray.GetAt","CHPtrArray::GetAt","GetAt","GetAt method [Windows Management Instrumentation]","GetAt method [Windows Management Instrumentation]","CHPtrArray interface","chptrarr/CHPtrArray::GetAt","wmi.chptrarray_getat"]
old-location: wmi\chptrarray_getat.htm
tech.root: wmi
ms.assetid: 7c2f029f-22a1-4433-971e-35ce48c004e0
ms.date: 12/05/2018
ms.keywords: ?GetAt@CHPtrArray@@QBEPAXH@Z, CHPtrArray interface [Windows Management Instrumentation],GetAt method, CHPtrArray.GetAt, CHPtrArray::GetAt, GetAt, GetAt method [Windows Management Instrumentation], GetAt method [Windows Management Instrumentation],CHPtrArray interface, chptrarr/CHPtrArray::GetAt, wmi.chptrarray_getat
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
 - CHPtrArray::GetAt
 - chptrarr/CHPtrArray::GetAt
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
 - CHPtrArray.GetAt
 - ?GetAt@CHPtrArray@@QBEPAXH@Z
---

# CHPtrArray::GetAt


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chptrarr/nl-chptrarr-chptrarray">CHPtrArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetAt</b> method accesses an element in a <a href="/windows/desktop/api/chptrarr/nl-chptrarr-chptrarray">CHPtrArray</a> array.

## -parameters

### -param nIndex

An integer index that is greater than or equal to zero (0), and less than or equal to the upper bound.

## -returns

If the <b>GetAt</b> method is successful, it returns the <a href="/windows/desktop/api/chptrarr/nl-chptrarr-chptrarray">CHPtrArray</a> pointer element currently at this index.

## -see-also

<a href="/windows/desktop/api/chptrarr/nl-chptrarr-chptrarray">CHPtrArray</a>



<a href="/windows/desktop/WmiSdk/provider-framework-utility-classes">Provider Framework Utility Classes</a>