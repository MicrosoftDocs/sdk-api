---
UID: NF:wbemtime.WBEMTime.operator-add
title: WBEMTime::operator-add (wbemtime.h)
description: The WBEMTime class addition operator (+) has been overloaded to increment an object's time by a time span.
helpviewer_keywords: ["??HWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z","WBEMTime interface [Windows Management Instrumentation]","operator+ method","WBEMTime.operator+","WBEMTime.operator-add","WBEMTime::operator+","WBEMTime::operator-add","_hmm_wbemtime_operator_plus","operator+","operator+ method [Windows Management Instrumentation]","operator+ method [Windows Management Instrumentation]","WBEMTime interface","wbemtime/WBEMTime::operator+","wmi.wbemtime_operator_plus"]
old-location: wmi\wbemtime_operator_plus.htm
tech.root: wmi
ms.assetid: d805f837-4063-4c16-aebc-88940a662d5e
ms.date: 12/05/2018
ms.keywords: ??HWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z, WBEMTime interface [Windows Management Instrumentation],operator+ method, WBEMTime.operator+, WBEMTime.operator-add, WBEMTime::operator+, WBEMTime::operator-add, _hmm_wbemtime_operator_plus, operator+, operator+ method [Windows Management Instrumentation], operator+ method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator+, wmi.wbemtime_operator_plus
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
 - WBEMTime::operator+
 - wbemtime/WBEMTime::operator+
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
 - WBEMTime.operator+
 - ??HWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z
---

# WBEMTime::operator-add


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class addition operator (+) has been overloaded to increment an object's time by a time span.

## -parameters

### -param uAdd [ref]

Reference to the <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object.

## -returns

A new <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object whose value is the sum of the "this" object and the <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> argument. The value of the "this" object is unchanged by this method.