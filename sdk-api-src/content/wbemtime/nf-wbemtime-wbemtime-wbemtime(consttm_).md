---
UID: NF:wbemtime.WBEMTime.WBEMTime(consttm&)
title: WBEMTime::WBEMTime(const tm &) (wbemtime.h)
description: The WBEMTime overload class constructor takes an ANSI C tm structure parameter.
helpviewer_keywords: ["??0WBEMTime@@QAE@ABUtm@@@Z","WBEMTime","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","WBEMTime constructor","WBEMTime.WBEMTime","WBEMTime.WBEMTime(const tm &)","WBEMTime::WBEMTime","WBEMTime::WBEMTime(const struct tm&)","WBEMTime::WBEMTime(const tm &)","wbemtime/WBEMTime::WBEMTime","wmi.wbemtime_wbemtime_const_struct_tm__"]
old-location: wmi\wbemtime_wbemtime_const_struct_tm__.htm
tech.root: wmi
ms.assetid: fe128577-0059-4728-9848-d947697bb386
ms.date: 12/05/2018
ms.keywords: ??0WBEMTime@@QAE@ABUtm@@@Z, WBEMTime, WBEMTime constructor [Windows Management Instrumentation], WBEMTime constructor [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],WBEMTime constructor, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const tm &), WBEMTime::WBEMTime, WBEMTime::WBEMTime(const struct tm&), WBEMTime::WBEMTime(const tm &), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime_const_struct_tm__
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
 - ??0WBEMTime@@QAE@ABUtm@@@Z
---

# WBEMTime::WBEMTime(const tm &)

## -description

[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries. The <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> overload class constructor takes an ANSI C <b>tm</b> structure parameter.

## -parameters

### -param tmin [ref]

ANSI C <b>tm</b> structure. A <b>tm</b> structure holds a time value using individual members and expressed as the number of years, months, day of month, hours, minutes, and seconds elapsed since 1900.