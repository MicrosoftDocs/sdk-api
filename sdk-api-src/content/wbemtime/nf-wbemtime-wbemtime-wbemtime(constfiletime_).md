---
UID: NF:wbemtime.WBEMTime.WBEMTime(constFILETIME&)
title: WBEMTime::WBEMTime(const FILETIME &) (wbemtime.h)
description: The WBEMTime overload class constructor takes a FILETIME reference parameter.
helpviewer_keywords: ["??0WBEMTime@@QAE@ABU_FILETIME@@@Z","??0WBEMTime@@QEAA@AEBU_FILETIME@@@Z","WBEMTime","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime constructor [Windows Management Instrumentation]","WBEMTime interface","WBEMTime interface [Windows Management Instrumentation]","WBEMTime constructor","WBEMTime.WBEMTime","WBEMTime.WBEMTime(const FILETIME &)","WBEMTime::WBEMTime","WBEMTime::WBEMTime(const FILETIME &)","WBEMTime::WBEMTime(const FILETIME&)","wbemtime/WBEMTime::WBEMTime","wmi.wbemtime_wbemtime_const_filetime__"]
old-location: wmi\wbemtime_wbemtime_const_filetime__.htm
tech.root: wmi
ms.assetid: 6538fee8-a807-45ce-abdf-1c20524d78f2
ms.date: 12/05/2018
ms.keywords: ??0WBEMTime@@QAE@ABU_FILETIME@@@Z, ??0WBEMTime@@QEAA@AEBU_FILETIME@@@Z, WBEMTime, WBEMTime constructor [Windows Management Instrumentation], WBEMTime constructor [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],WBEMTime constructor, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const FILETIME &), WBEMTime::WBEMTime, WBEMTime::WBEMTime(const FILETIME &), WBEMTime::WBEMTime(const FILETIME&), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime_const_filetime__
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
 - ??0WBEMTime@@QAE@ABU_FILETIME@@@Z
 - ??0WBEMTime@@QEAA@AEBU_FILETIME@@@Z
---

# WBEMTime::WBEMTime(const FILETIME &)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a>  overload class constructor  takes a FILETIME reference parameter.

## -parameters

### -param ft [ref]

MFC <b>FILETIME</b> structure that represents the number of 100-nanosecond intervals since January 1, 1601, as a 64-bit value.