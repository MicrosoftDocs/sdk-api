---
UID: NL:wbemtime.WBEMTimeSpan
title: WBEMTimeSpan (wbemtime.h)
description: The WBEMTimeSpan class holds time spans in nanoseconds.
helpviewer_keywords: ["WBEMTimeSpan","WBEMTimeSpan class [Windows Management Instrumentation]","WBEMTimeSpan class [Windows Management Instrumentation]","described","_hmm_wbemtimespan","wbemtime/WBEMTimeSpan","wmi.wbemtimespan"]
old-location: wmi\wbemtimespan.htm
tech.root: wmi
ms.assetid: bcec87c1-32ba-451b-92bb-80c8a5007adb
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan, WBEMTimeSpan class [Windows Management Instrumentation], WBEMTimeSpan class [Windows Management Instrumentation],described, _hmm_wbemtimespan, wbemtime/WBEMTimeSpan, wmi.wbemtimespan
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
 - WBEMTimeSpan
 - wbemtime/WBEMTimeSpan
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
 - WBEMTimeSpan
---

# WBEMTimeSpan class


## -description

<p class="CCE_Message">[The <b>WBEMTimeSpan</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTimeSpan</b> class holds time spans in nanoseconds.<b>WBEMTimeSpan</b> objects can result from the arithmetic manipulation of <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> objects. For example, subtracting one <b>WBEMTime</b> object from another results in a <b>WBEMTimeSpan</b> object that represents the difference in time between the two objects. Instances of <b>WBEMTimeSpan</b> can also be used to wrap any data that has an inherent duration, such as the time that remains until a password expires.


## -see-also

<a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime Class Methods</a>
