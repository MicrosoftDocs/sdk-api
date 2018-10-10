---
UID: NF:wbemtime.WBEMTime.operator-equal-equal-to
title: WBEMTime::operator-equal-equal-to
author: windows-sdk-content
description: The WBEMTime comparison operators (== != &lt; &lt;= &gt; &gt;=) have been overloaded to compare two WBEMTime objects.
old-location: wmi\wbemtime_comparison_operators_equal.htm
tech.root: WmiSdk
ms.assetid: 9060553a-db93-44c3-ae64-1e14c5087485
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator== method, WBEMTime.operator-equal-equal-to, WBEMTime.operator==, WBEMTime::operator-equal-equal-to, WBEMTime::operator==, _hmm_wbemtime_comparison_operators, operator==, operator== method [Windows Management Instrumentation], operator== method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator==, wmi.wbemtime_comparison_operators, wmi.wbemtime_comparison_operators_equal
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
 - WBEMTime.operator==
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTime::operator-equal-equal-to


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> comparison operators (== != &lt; &lt;= &gt; &gt;=) have been overloaded to compare two <b>WBEMTime</b> objects.


## -parameters




### -param a

TBD




#### - uTarget [ref]

Reference to the <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object whose time is compared to this one.


## -returns



True if this time and the time specified by <i>uTarget</i> are identical.



