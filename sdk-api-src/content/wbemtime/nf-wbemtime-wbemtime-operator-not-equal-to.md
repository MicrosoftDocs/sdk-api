---
UID: NF:wbemtime.WBEMTime.operator-not-equal-to
title: WBEMTime::operator-not-equal-to (wbemtime.h)
description: The WBEMTime::operator-not-equal-to (wbemtime.h) comparison operators (== != &lt; &lt;= &gt; &gt;=) have been overloaded to compare two WBEMTime objects.
helpviewer_keywords: ["WBEMTime interface [Windows Management Instrumentation]","operator!= method","WBEMTime.operator!=","WBEMTime.operator-not-equal-to","WBEMTime::operator!=","WBEMTime::operator-not-equal-to","operator!=","operator!= method [Windows Management Instrumentation]","operator!= method [Windows Management Instrumentation]","WBEMTime interface","wbemtime/WBEMTime::operator!=","wmi.wbemtime_comparison_operators_notequal"]
old-location: wmi\wbemtime_comparison_operators_notequal.htm
tech.root: wmi
ms.assetid: 9fdd37ed-a6b3-4cc0-8e0b-684265647051
ms.date: 08/15/2022
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator!= method, WBEMTime.operator!=, WBEMTime.operator-not-equal-to, WBEMTime::operator!=, WBEMTime::operator-not-equal-to, operator!=, operator!= method [Windows Management Instrumentation], operator!= method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator!=, wmi.wbemtime_comparison_operators_notequal
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
 - WBEMTime::operator!=
 - wbemtime/WBEMTime::operator!=
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
 - WBEMTime.operator!=
---

# WBEMTime::operator-not-equal-to


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> comparison operators (== != &lt; &lt;= &gt; &gt;=) have been overloaded to compare two <b>WBEMTime</b> objects.

## -parameters

### -param a [ref]

Reference to the <a href="/windows/desktop/WmiSdk/wbemtime">WBEMTime</a> object whose time is compared to this one.

## -returns

True if this time and the time specified by <i>uTarget</i> are different.
