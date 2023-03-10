---
UID: NF:wbemtime.WBEMTime.GetSYSTEMTIME
title: WBEMTime::GetSYSTEMTIME (wbemtime.h)
description: The GetSYSTEMTIME method gets the time as an MFC SYSTEMTIME structure.
helpviewer_keywords: ["?GetSYSTEMTIME@WBEMTime@@QBEHPAU_SYSTEMTIME@@@Z","?GetSYSTEMTIME@WBEMTime@@QEBAHPEAU_SYSTEMTIME@@@Z","GetSYSTEMTIME","GetSYSTEMTIME method [Windows Management Instrumentation]","GetSYSTEMTIME method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetSYSTEMTIME method","WBEMTime.GetSYSTEMTIME","WBEMTime::GetSYSTEMTIME","_hmm_wbemtime_getsystemtime","wbemtime/WBEMTime::GetSYSTEMTIME","wmi.wbemtime_getsystemtime"]
old-location: wmi\wbemtime_getsystemtime.htm
tech.root: wmi
ms.assetid: e65cc4e2-36d3-43de-be65-f48ddfb0b273
ms.date: 12/05/2018
ms.keywords: ?GetSYSTEMTIME@WBEMTime@@QBEHPAU_SYSTEMTIME@@@Z, ?GetSYSTEMTIME@WBEMTime@@QEBAHPEAU_SYSTEMTIME@@@Z, GetSYSTEMTIME, GetSYSTEMTIME method [Windows Management Instrumentation], GetSYSTEMTIME method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetSYSTEMTIME method, WBEMTime.GetSYSTEMTIME, WBEMTime::GetSYSTEMTIME, _hmm_wbemtime_getsystemtime, wbemtime/WBEMTime::GetSYSTEMTIME, wmi.wbemtime_getsystemtime
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
 - WBEMTime::GetSYSTEMTIME
 - wbemtime/WBEMTime::GetSYSTEMTIME
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
 - WBEMTime.GetSYSTEMTIME
 - ?GetSYSTEMTIME@WBEMTime@@QBEHPAU_SYSTEMTIME@@@Z
 - ?GetSYSTEMTIME@WBEMTime@@QEBAHPEAU_SYSTEMTIME@@@Z
---

# WBEMTime::GetSYSTEMTIME


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetSYSTEMTIME</b> method gets the time as an MFC <b>SYSTEMTIME</b> structure.

## -parameters

### -param pst

Pointer to a MFC <b>SYSTEMTIME</b> structure. The <b>SYSTEMTIME</b> structure represents a date and time using individual members for the month, day, year, weekday, hour, minute, second, and millisecond.

## -returns

The method returns <b>TRUE</b> if the time is valid.

The method returns <b>FALSE</b> if the time is INVALID_TIME. In this case, the value of <i>pst</i> is indeterminate.