---
UID: NF:wbemtime.WBEMTimeSpan.operator-greater-than
title: WBEMTimeSpan::operator-greater-than (wbemtime.h)
author: windows-sdk-content
description: Compares two WBEMTimeSpan objects using a greater than comparison operator.
old-location: wmi\wbemtimespan_comparison_operators_greaterthan.htm
tech.root: WmiSdk
ms.assetid: 579e0041-0e33-4367-923d-15b59eee4cae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "??OWBEMTimeSpan@@QBEHABV0@@Z, WBEMTimeSpan interface [Windows Management Instrumentation],operator> method, WBEMTimeSpan.operator-greater-than, WBEMTimeSpan.operator>, WBEMTimeSpan::operator-greater-than, WBEMTimeSpan::operator>, operator>, operator> method [Windows Management Instrumentation], operator> method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator>, wmi.wbemtimespan_comparison_operators_greaterthan"
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
 - WBEMTimeSpan.operator>
 - ??OWBEMTimeSpan@@QBEHABV0@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTimeSpan::operator-greater-than


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Compares two <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> objects using a greater than comparison operator.


## -parameters




### -param a [ref]

Reference to the <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object, whose time span is compared to this one.


## -returns



<b>TRUE</b> if this time span is greater than the time span specified by <i>uTarget</i>.



