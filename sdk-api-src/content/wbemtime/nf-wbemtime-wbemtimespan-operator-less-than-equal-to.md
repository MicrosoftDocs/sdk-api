---
UID: NF:wbemtime.WBEMTimeSpan.operator-less-than-equal-to
title: WBEMTimeSpan::operator-less-than-equal-to
author: windows-sdk-content
description: Compares two WBEMTimeSpan objects using a less than or equal comparison operator.
old-location: wmi\wbemtimespan_comparison_operators_lessthanorequal.htm
tech.root: WmiSdk
ms.assetid: 32fdd62d-1f48-4cf7-824e-18edf4fd7b95
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator<= method, WBEMTimeSpan.operator-less-than-equal-to, WBEMTimeSpan.operator<=, WBEMTimeSpan::operator-less-than-equal-to, WBEMTimeSpan::operator<=, operator<=, operator<= method [Windows Management Instrumentation], operator<= method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator<=, wmi.wbemtimespan_comparison_operators_lessthanorequal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - WBEMTimeSpan.operator<=
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTimeSpan::operator-less-than-equal-to


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa393989(v=VS.85).aspx">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Compares two <a href="https://msdn.microsoft.com/en-us/library/Aa393989(v=VS.85).aspx">WBEMTimeSpan</a> objects using a less than or equal comparison operator.


## -parameters




### -param a [ref]

Reference to the <a href="https://msdn.microsoft.com/en-us/library/Aa393989(v=VS.85).aspx">WBEMTimeSpan</a> object whose time span is compared to this one.


## -returns



<b>TRUE</b> if this time span is less than or equal to the time span specified by <i>uTarget</i>.



