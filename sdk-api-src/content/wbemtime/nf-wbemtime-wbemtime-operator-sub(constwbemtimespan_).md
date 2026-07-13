---
UID: NF:wbemtime.WBEMTime.operator-sub(constWBEMTimeSpan&)
title: WBEMTime::operator-sub(const WBEMTimeSpan &) (wbemtime.h)
description: This overload of the WBEMTime class subtraction operator (—) subtracts a time span from an object's time to produce a new time object that contains the resulting time. (overload 1/2)
helpviewer_keywords: ["??GWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z","WBEMTime interface [Windows Management Instrumentation]","operator- method","WBEMTime.operator-","WBEMTime.operator-sub(const WBEMTimeSpan &)","WBEMTime::operator-","WBEMTime::operator-(const WBEMTimeSpan&)","WBEMTime::operator-sub(const WBEMTimeSpan &)","operator-","operator- method [Windows Management Instrumentation]","operator- method [Windows Management Instrumentation]","WBEMTime interface","wbemtime/WBEMTime::operator-","wmi.wbemtime_operator_minus_const_wbemtimespan__"]
old-location: wmi\wbemtime_operator_minus_const_wbemtimespan__.htm
tech.root: wmi
ms.assetid: d96efdf3-1020-4145-92ad-bbde5704639e
ms.date: 12/05/2018
ms.keywords: ??GWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z, WBEMTime interface [Windows Management Instrumentation],operator- method, WBEMTime.operator-, WBEMTime.operator-sub(const WBEMTimeSpan &), WBEMTime::operator-, WBEMTime::operator-(const WBEMTimeSpan&), WBEMTime::operator-sub(const WBEMTimeSpan &), operator-, operator- method [Windows Management Instrumentation], operator- method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator-, wmi.wbemtime_operator_minus_const_wbemtimespan__
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
 - WBEMTime::operator-
 - wbemtime/WBEMTime::operator-
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
 - WBEMTime.operator-
 - ??GWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z
---

# WBEMTime::operator-sub(const WBEMTimeSpan &)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

This overload of the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class subtraction operator (–) subtracts a time span from an object's time to produce a new time object that contains the resulting time.

## -parameters

### -param sub [ref]

Reference to the <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object whose time span is subtracted from the "this" object.

## -returns

When a <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object is returned, it is a new object whose time is the difference between the "this" object and the <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object used as the argument.

When a <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object is returned, it is a new time span object whose value is the difference between the "this" object and the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object used as an argument.

Any returned objects that has a negative time span or a time before Jan 1, 1601 is set to INVALID_TIME.
