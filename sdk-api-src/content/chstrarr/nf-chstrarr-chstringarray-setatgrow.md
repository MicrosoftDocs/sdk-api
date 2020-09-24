---
UID: NF:chstrarr.CHStringArray.SetAtGrow
title: CHStringArray::SetAtGrow (chstrarr.h)
description: Sets the array element at the specified index.
helpviewer_keywords: ["CHStringArray interface [Windows Management Instrumentation]","SetAtGrow method","CHStringArray.SetAtGrow","CHStringArray::SetAtGrow","SetAtGrow","SetAtGrow method [Windows Management Instrumentation]","SetAtGrow method [Windows Management Instrumentation]","CHStringArray interface","_hmm_chstringarray_setatgrow","chstrarr/CHStringArray::SetAtGrow","wmi.chstringarray_setatgrow"]
old-location: wmi\chstringarray_setatgrow.htm
tech.root: wmi
ms.assetid: 49cc7e6f-2d15-4756-bffd-e21f38b8ce8b
ms.date: 12/05/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],SetAtGrow method, CHStringArray.SetAtGrow, CHStringArray::SetAtGrow, SetAtGrow, SetAtGrow method [Windows Management Instrumentation], SetAtGrow method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_setatgrow, chstrarr/CHStringArray::SetAtGrow, wmi.chstringarray_setatgrow
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
 - CHStringArray::SetAtGrow
 - chstrarr/CHStringArray::SetAtGrow
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
 - CHStringArray.SetAtGrow
---

# CHStringArray::SetAtGrow


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetAtGrow</b> method sets the array element at the specified index. The array increases automatically if necessary, adjusting the upper bound to accommodate the new element.

## -parameters

### -param nIndex

An integer index that is greater than or equal to zero (0).

<div class="alert"><b>Note</b>  The <i>nIndex</i> parameter must be greater than or equal to zero (0). The debug version of the <a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a> library validates the bounds of <i>nIndex</i>; the release version does not.</div>
<div> </div>

### -param newElement

The object pointer to be added to this array. A <b>NULL</b> value is allowed.

## -returns

This method does not return a value.

## -see-also

<a href="/windows/desktop/api/chstrarr/nl-chstrarr-chstringarray">CHStringArray</a>



<a href="/windows/desktop/api/chstrarr/nf-chstrarr-chstringarray-setat(int_lpcwstr)">CHStringArray::SetAt</a>



<a href="/windows/desktop/WmiSdk/chstringarray--operator-brackets">CHStringArray::operator []</a>