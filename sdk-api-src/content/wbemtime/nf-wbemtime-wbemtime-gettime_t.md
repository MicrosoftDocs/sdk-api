---
UID: NF:wbemtime.WBEMTime.Gettime_t
title: WBEMTime::Gettime_t (wbemtime.h)
description: The Gettime_t method gets the time as an ANSI C run-time time_t variable.
helpviewer_keywords: ["?Gettime_t@WBEMTime@@QBEHPAJ@Z","Gettime_t","Gettime_t method [Windows Management Instrumentation]","Gettime_t method [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","Gettime_t method","WBEMTime.Gettime_t","WBEMTime::Gettime_t","_hmm_wbemtime_gettime_t","wbemtime/WBEMTime::Gettime_t","wmi.wbemtime_gettime_t"]
old-location: wmi\wbemtime_gettime_t.htm
tech.root: wmi
ms.assetid: 62e0faff-4e5a-4bc4-a9a7-a4edbaea9541
ms.date: 12/05/2018
ms.keywords: ?Gettime_t@WBEMTime@@QBEHPAJ@Z, Gettime_t, Gettime_t method [Windows Management Instrumentation], Gettime_t method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],Gettime_t method, WBEMTime.Gettime_t, WBEMTime::Gettime_t, _hmm_wbemtime_gettime_t, wbemtime/WBEMTime::Gettime_t, wmi.wbemtime_gettime_t
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
 - WBEMTime::Gettime_t
 - wbemtime/WBEMTime::Gettime_t
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
 - WBEMTime.Gettime_t
 - ?Gettime_t@WBEMTime@@QBEHPAJ@Z
---

# WBEMTime::Gettime_t


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Gettime_t</b> method gets the time as an ANSI C run-time <b>time_t</b> variable.

## -parameters

### -param ptime_t

ANSI C run-time <b>time_t</b> variable, which represents the number of seconds since midnight Jan 1, 1970. In DMTF format, this is 19700101000000.000000-000.

## -returns

The method returns <b>TRUE</b> if the object's time is equal to or later than midnight Jan 1, 1970.

The method returns <b>FALSE</b> on all other times or if the object's time is set to INVALID_TIME. In this case, the value of <i>ptm</i> is indeterminate.