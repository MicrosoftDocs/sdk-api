---
UID: NF:wbemtime.WBEMTimeSpan.operator-less-than
title: WBEMTimeSpan::operator-less-than (wbemtime.h)
description: Compares two WBEMTimeSpan objects using a less than comparison operator.
helpviewer_keywords: ["WBEMTimeSpan interface [Windows Management Instrumentation]","operator< method","WBEMTimeSpan.operator-less-than","WBEMTimeSpan.operator<","WBEMTimeSpan::operator-less-than","WBEMTimeSpan::operator<","operator<","operator< method [Windows Management Instrumentation]","operator< method [Windows Management Instrumentation]","WBEMTimeSpan interface","wbemtime/WBEMTimeSpan::operator<","wmi.wbemtimespan_comparison_operators_lessthan"]
old-location: wmi\wbemtimespan_comparison_operators_lessthan.htm
tech.root: wmi
ms.assetid: c26d360f-32e7-4cbd-ad39-0997590a8d32
ms.date: 12/05/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator< method, WBEMTimeSpan.operator-less-than, WBEMTimeSpan.operator<, WBEMTimeSpan::operator-less-than, WBEMTimeSpan::operator<, operator<, operator< method [Windows Management Instrumentation], operator< method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator<, wmi.wbemtimespan_comparison_operators_lessthan
f1_keywords:
- wbemtime/WBEMTimeSpan.operator<
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- WBEMTimeSpan.operator<
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WBEMTimeSpan::operator-less-than


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Compares two <a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> objects using a less than comparison operator.


## -parameters




### -param a [ref]

Reference to the <a href="https://docs.microsoft.com/windows/desktop/api/wbemtime/nl-wbemtime-wbemtimespan">WBEMTimeSpan</a> object, whose time span is compared to this one.


## -returns



<b>TRUE</b> if this time span is less than the time span specified by <i>uTarget</i>.



