---
UID: NF:wbemtime.WBEMTime.WBEMTime(consttime_t&)
title: WBEMTime::WBEMTime(const time_t &) (wbemtime.h)
description: The WBEMTime overload class constructor takes an ANSI C time_t structure parameter.
helpviewer_keywords: ["WBEMTime","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","WBEMTime constructor","WBEMTime.WBEMTime","WBEMTime.WBEMTime(const time_t &)","WBEMTime::WBEMTime","WBEMTime::WBEMTime(const time_t &)","WBEMTime::WBEMTime(const time_t&)","wbemtime/WBEMTime::WBEMTime","wmi.wbemtime_wbemtime_const_time_t__"]
old-location: wmi\wbemtime_wbemtime_const_time_t__.htm
tech.root: wmi
ms.assetid: be698827-c9dc-4f30-9962-2e3f5f2bd029
ms.date: 12/05/2018
ms.keywords: WBEMTime, WBEMTime constructor [Windows Management Instrumentation], WBEMTime constructor [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],WBEMTime constructor, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const time_t &), WBEMTime::WBEMTime, WBEMTime::WBEMTime(const time_t &), WBEMTime::WBEMTime(const time_t&), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime_const_time_t__
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
 - WBEMTime::WBEMTime
 - wbemtime/WBEMTime::WBEMTime
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
 - WBEMTime.WBEMTime
---

# WBEMTime::WBEMTime(const time_t &)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> overload class constructor takes an ANSI C <b>time_t</b> structure parameter.

## -parameters

### -param t [ref]

ANSI C <b>time_t</b> structure that holds the number of seconds since midnight Jan 1, 1970 (CIM format: 19700101000000.000000-000). For more information, see <a href="/windows/desktop/WmiSdk/date-and-time-format">Date and Time Format</a>.