---
UID: NF:wbemtime.WBEMTimeSpan.operator-sub-assign
title: WBEMTimeSpan::operator-sub-assign (wbemtime.h)
description: Compares two WBEMTimeSpan objects using the subtract and assign operator (—=).
helpviewer_keywords: ["WBEMTimeSpan interface [Windows Management Instrumentation]","operator-= method","WBEMTimeSpan.operator-=","WBEMTimeSpan.operator-sub-assign","WBEMTimeSpan::operator-=","WBEMTimeSpan::operator-sub-assign","_hmm_wbemtimespan_operator_minus_equal","operator-=","operator-= method [Windows Management Instrumentation]","operator-= method [Windows Management Instrumentation]","WBEMTimeSpan interface","wbemtime/WBEMTimeSpan::operator-=","wmi.wbemtimespan_operator_minus_equal"]
old-location: wmi\wbemtimespan_operator_minus_equal.htm
tech.root: wmi
ms.assetid: 4cf466bc-278e-4352-a818-ed74ff65903a
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator-= method, WBEMTimeSpan.operator-=, WBEMTimeSpan.operator-sub-assign, WBEMTimeSpan::operator-=, WBEMTimeSpan::operator-sub-assign, _hmm_wbemtimespan_operator_minus_equal, operator-=, operator-= method [Windows Management Instrumentation], operator-= method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator-=, wmi.wbemtimespan_operator_minus_equal
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
 - WBEMTimeSpan::operator-=
 - wbemtime/WBEMTimeSpan::operator-=
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
 - WBEMTimeSpan.operator-=
---

# WBEMTimeSpan::operator-sub-assign


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Compares two <b>WBEMTimeSpan</b> objects using the subtract and assign operator (–=).

## -parameters

### -param uSub [ref]

Reference to the <b>WBEMTimeSpan</b> object, whose time span is subtracted from the "this" object.

## -returns

This method returns a new <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object with a value equal to the difference in time.