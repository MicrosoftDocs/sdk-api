---
UID: NF:wbemtime.WBEMTime.WBEMTime(constSYSTEMTIME&)
title: WBEMTime::WBEMTime(const SYSTEMTIME &) (wbemtime.h)
description: The WBEMTime overload class constructor takes a SYSTEMTIME parameter.
helpviewer_keywords: ["??0WBEMTime@@QAE@ABU_SYSTEMTIME@@@Z","??0WBEMTime@@QEAA@AEBU_SYSTEMTIME@@@Z","WBEMTime","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","WBEMTime constructor","WBEMTime.WBEMTime","WBEMTime.WBEMTime(const SYSTEMTIME &)","WBEMTime::WBEMTime","WBEMTime::WBEMTime(const SYSTEMTIME &)","WBEMTime::WBEMTime(const SYSTEMTIME&)","wbemtime/WBEMTime::WBEMTime","wmi.wbemtime_wbemtime_const_systemtime__"]
old-location: wmi\wbemtime_wbemtime_const_systemtime__.htm
tech.root: wmi
ms.assetid: 02bc92e3-17cd-4102-bbaa-cc3216b426ff
ms.date: 12/05/2018
ms.keywords: ??0WBEMTime@@QAE@ABU_SYSTEMTIME@@@Z, ??0WBEMTime@@QEAA@AEBU_SYSTEMTIME@@@Z, WBEMTime, WBEMTime constructor [Windows Management Instrumentation], WBEMTime constructor [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],WBEMTime constructor, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const SYSTEMTIME &), WBEMTime::WBEMTime, WBEMTime::WBEMTime(const SYSTEMTIME &), WBEMTime::WBEMTime(const SYSTEMTIME&), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime_const_systemtime__
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
 - ??0WBEMTime@@QAE@ABU_SYSTEMTIME@@@Z
 - ??0WBEMTime@@QEAA@AEBU_SYSTEMTIME@@@Z
---

# WBEMTime::WBEMTime(const SYSTEMTIME &)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> overload class constructor takes a <b>SYSTEMTIME</b> parameter.

## -parameters

### -param st [ref]

MFC <b>SYSTEMTIME</b> structure that represents a date and time and using individual members for the month, day, year, weekday, hour, minute, second, and millisecond.