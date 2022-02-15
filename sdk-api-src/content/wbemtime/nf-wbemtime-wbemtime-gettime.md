---
UID: NF:wbemtime.WBEMTime.GetTime
title: WBEMTime::GetTime (wbemtime.h)
description: The GetTime method returns the time as a 64-bit integer.
helpviewer_keywords: ["GetTime","GetTime method [Windows Management Instrumentation]","GetTime method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","GetTime method","WBEMTime.GetTime","WBEMTime::GetTime","_hmm_wbemtime_gettime","wbemtime/WBEMTime::GetTime","wmi.wbemtime_gettime"]
old-location: wmi\wbemtime_gettime.htm
tech.root: wmi
ms.assetid: 1690d33d-c39b-448e-889e-48dce1933fc1
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [Windows Management Instrumentation], GetTime method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetTime method, WBEMTime.GetTime, WBEMTime::GetTime, _hmm_wbemtime_gettime, wbemtime/WBEMTime::GetTime, wmi.wbemtime_gettime
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
 - WBEMTime::GetTime
 - wbemtime/WBEMTime::GetTime
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
 - WBEMTime.GetTime
---

# WBEMTime::GetTime


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetTime</b> method returns the time as a 64-bit integer.



## -returns

Returns the time as a GMT <b>FILETIME</b> structure. If the time is invalid, it returns INVALID_TIME.

## -remarks

The method is provided to assist users in debugging.
