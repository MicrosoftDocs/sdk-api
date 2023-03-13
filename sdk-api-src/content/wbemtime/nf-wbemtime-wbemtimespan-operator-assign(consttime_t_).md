---
UID: NF:wbemtime.WBEMTimeSpan.operator-assign(consttime_t&)
title: WBEMTimeSpan::operator-assign(const time_t &) (wbemtime.h)
description: Converts a BSTR time interval value to a WBEMTimeSpan object in CIM date and time format. (overload 3/3)
helpviewer_keywords: ["WBEMTimeSpan interface [Windows Management Instrumentation]","operator= method","WBEMTimeSpan.operator-assign(const time_t &)","WBEMTimeSpan.operator=","WBEMTimeSpan::operator-assign(const time_t &)","WBEMTimeSpan::operator=","_hmm_wbemtimespan_operator_equal","operator=","operator= method [Windows Management Instrumentation]","operator= method [Windows Management Instrumentation]","WBEMTimeSpan interface","wbemtime/WBEMTimeSpan::operator=","wmi.wbemtimespan_operator_equal"]
old-location: wmi\wbemtimespan_operator_equal.htm
tech.root: wmi
ms.assetid: e97bf5c7-90fd-49a7-9c3c-c719d5374f84
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator= method, WBEMTimeSpan.operator-assign(const time_t &), WBEMTimeSpan.operator=, WBEMTimeSpan::operator-assign(const time_t &), WBEMTimeSpan::operator=, _hmm_wbemtimespan_operator_equal, operator=, operator= method [Windows Management Instrumentation], operator= method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator=, wmi.wbemtimespan_operator_equal
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
 - WBEMTimeSpan::operator=
 - wbemtime/WBEMTimeSpan::operator=
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
 - WBEMTimeSpan.operator=
---

# WBEMTimeSpan::operator-assign(const time_t &)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Converts a <b>BSTR</b> time interval value to a <a href="/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object in CIM <a href="/windows/desktop/WmiSdk/date-and-time-format">date and time format</a>.

## -parameters

### -param t

<b>BSTR</b> in <a href="/windows/desktop/WmiSdk/interval-format">Interval Format</a>.
