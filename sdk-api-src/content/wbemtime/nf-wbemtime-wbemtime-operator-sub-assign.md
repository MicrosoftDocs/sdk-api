---
UID: NF:wbemtime.WBEMTime.operator-sub-assign
title: WBEMTime::operator-sub-assign (wbemtime.h)
description: The WBEMTime class subtract-and-assign (—=) operator has been overloaded to decrement an object's time by a time span.
helpviewer_keywords: ["WBEMTime interface [Windows Management Instrumentation]","operator-= method","WBEMTime.operator-=","WBEMTime.operator-sub-assign","WBEMTime::operator-=","WBEMTime::operator-sub-assign","_hmm_wbemtime_operator_minus_equal","operator-=","operator-= method [Windows Management Instrumentation]","operator-= method [Windows Management Instrumentation]","WBEMTime interface","wbemtime/WBEMTime::operator-=","wmi.wbemtime_operator_minus_equal"]
old-location: wmi\wbemtime_operator_minus_equal.htm
tech.root: wmi
ms.assetid: 842cfddd-f137-46ba-9744-e3a71dd82f01
ms.date: 12/05/2018
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator-= method, WBEMTime.operator-=, WBEMTime.operator-sub-assign, WBEMTime::operator-=, WBEMTime::operator-sub-assign, _hmm_wbemtime_operator_minus_equal, operator-=, operator-= method [Windows Management Instrumentation], operator-= method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator-=, wmi.wbemtime_operator_minus_equal
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
 - WBEMTime::operator-=
 - wbemtime/WBEMTime::operator-=
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
 - WBEMTime.operator-=
---

# WBEMTime::operator-sub-assign


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class subtract-and-assign (–=) operator has been overloaded to decrement an object's time by a time span.

## -parameters

### -param sub [ref]

Reference to the <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object, whose time span is subtracted from the specified object.

## -remarks

The return value is a new <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object with a value equal to the "this" object after it has been decremented.