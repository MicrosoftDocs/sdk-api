---
UID: NF:wbemtime.WBEMTimeSpan.operator-add
title: WBEMTimeSpan::operator-add (wbemtime.h)
description: The WBEMTimeSpan class add operator adds one time span to another, placing the sum in a new WBEMTimeSpan object returned by the method.
helpviewer_keywords: ["WBEMTimeSpan interface [Windows Management Instrumentation]","operator+ method","WBEMTimeSpan.operator+","WBEMTimeSpan.operator-add","WBEMTimeSpan::operator+","WBEMTimeSpan::operator-add","_hmm_wbemtimespan_operator_plus","operator+","operator+ method [Windows Management Instrumentation]","operator+ method [Windows Management Instrumentation]","WBEMTimeSpan interface","wbemtime/WBEMTimeSpan::operator+","wmi.wbemtimespan_operator_plus"]
old-location: wmi\wbemtimespan_operator_plus.htm
tech.root: wmi
ms.assetid: 48e0fcbe-a8a0-4193-b55f-ed4bb7d98614
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator+ method, WBEMTimeSpan.operator+, WBEMTimeSpan.operator-add, WBEMTimeSpan::operator+, WBEMTimeSpan::operator-add, _hmm_wbemtimespan_operator_plus, operator+, operator+ method [Windows Management Instrumentation], operator+ method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator+, wmi.wbemtimespan_operator_plus
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
 - WBEMTimeSpan::operator+
 - wbemtime/WBEMTimeSpan::operator+
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
 - WBEMTimeSpan.operator+
---

# WBEMTimeSpan::operator-add


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTimeSpan</b> class add operator adds one time span to another, placing the sum in a new <b>WBEMTimeSpan</b> object returned by the method.

## -parameters

### -param uAdd [ref]

Reference to a <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object, whose time span is added to this one.

## -returns

The method returns a new <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object, whose time span is equal to the sum of its two <b>WBEMTimeSpan</b> arguments.