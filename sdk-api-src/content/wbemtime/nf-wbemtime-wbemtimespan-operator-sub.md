---
UID: NF:wbemtime.WBEMTimeSpan.operator-sub
title: WBEMTimeSpan::operator-sub (wbemtime.h)
description: The WBEMTimeSpan class subtract operator (—) subtracts a time span from the object on which the method is executed.
helpviewer_keywords: ["WBEMTimeSpan interface [Windows Management Instrumentation]","operator- method","WBEMTimeSpan.operator-","WBEMTimeSpan.operator-sub","WBEMTimeSpan::operator-","WBEMTimeSpan::operator-sub","_hmm_wbemtimespan_operator_minus","operator-","operator- method [Windows Management Instrumentation]","operator- method [Windows Management Instrumentation]","WBEMTimeSpan interface","wbemtime/WBEMTimeSpan::operator-","wmi.wbemtimespan_operator_minus"]
old-location: wmi\wbemtimespan_operator_minus.htm
tech.root: wmi
ms.assetid: 643e3353-c770-46e6-aa59-b6df43097988
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator- method, WBEMTimeSpan.operator-, WBEMTimeSpan.operator-sub, WBEMTimeSpan::operator-, WBEMTimeSpan::operator-sub, _hmm_wbemtimespan_operator_minus, operator-, operator- method [Windows Management Instrumentation], operator- method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator-, wmi.wbemtimespan_operator_minus
req.header: wbemtime.h
req.include-header: 
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
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WBEMTimeSpan::operator-
 - wbemtime/WBEMTimeSpan::operator-
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
 - WBEMTimeSpan.operator-
---

# WBEMTimeSpan::operator-sub


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTimeSpan</b> class subtract operator (–) subtracts a time span from the object on which the method is executed.  The result is  a new time span that contains the difference in time.

## -parameters

### -param uSub [ref]

Reference to the <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object, whose time span is subtracted from this time span, producing a new time span.

## -returns

This method returns a new <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object with a value equal to the difference in time.

<div class="alert"><b>Note</b>  The new time span is set to INVALID_TIME if a negative time span results. Subtracting a time span from an object that contains INVALID_TIME produces a new time span object set to INVALID_TIME.</div>
<div> </div>