---
UID: NF:wbemtime.WBEMTime.operator-greater-than-equal-to
title: WBEMTime::operator-greater-than-equal-to (wbemtime.h)
description: The WBEMTime::operator-greater-than-equal-to (wbemtime.h) comparison operators (== != &lt; &lt;= &gt; &gt;=) have been overloaded to compare two WBEMTime objects.
helpviewer_keywords: ["WBEMTime interface [Windows Management Instrumentation]","operator>= method","WBEMTime.operator-greater-than-equal-to","WBEMTime.operator>=","WBEMTime::operator-greater-than-equal-to","WBEMTime::operator>=","operator>=","operator>= method [Windows Management Instrumentation]","operator>= method [Windows Management Instrumentation]","WBEMTime interface","wbemtime/WBEMTime::operator>=","wmi.wbemtime_comparison_operators_greaterthanorequal"]
old-location: wmi\wbemtime_comparison_operators_greaterthanorequal.htm
tech.root: wmi
ms.assetid: e483efa0-e0d9-4ebf-bac5-831960de0146
ms.date: 08/15/2022
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator>= method, WBEMTime.operator-greater-than-equal-to, WBEMTime.operator>=, WBEMTime::operator-greater-than-equal-to, WBEMTime::operator>=, operator>=, operator>= method [Windows Management Instrumentation], operator>= method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator>=, wmi.wbemtime_comparison_operators_greaterthanorequal
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
 - WBEMTime::operator>=
 - wbemtime/WBEMTime::operator>=
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
 - WBEMTime.operator>=
---

# WBEMTime::operator-greater-than-equal-to


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

True if this time is greater than or equal to the time specified by <i>uTarget</i>.
