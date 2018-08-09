---
UID: NF:wbemtime.WBEMTime.operator-(const WBEMTimeSpan &)
title: WBEMTime::operator-(const WBEMTimeSpan &)
author: windows-sdk-content
description: This overload of the WBEMTime class subtraction operator (&#8211;) subtracts a time span from an object's time to produce a new time object that contains the resulting time.
old-location: wmi\wbemtime_operator_minus_const_wbemtimespan__.htm
old-project: WmiSdk
ms.assetid: d96efdf3-1020-4145-92ad-bbde5704639e
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "??GWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z, WBEMTime interface [Windows Management Instrumentation],operator- method, WBEMTime.operator-, WBEMTime.operator-(const WBEMTimeSpan &), WBEMTime::operator-, WBEMTime::operator-(const WBEMTimeSpan &), WBEMTime::operator-(const WBEMTimeSpan&), operator-, operator- method [Windows Management Instrumentation], operator- method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator-, wmi.wbemtime_operator_minus_const_wbemtimespan__"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - WBEMTime.operator-
 - ??GWBEMTime@@QBE?AV0@ABVWBEMTimeSpan@@@Z
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::operator-(const WBEMTimeSpan &)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

This overload of the <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class subtraction operator (–) subtracts a time span from an object's time to produce a new time object that contains the resulting time.


## -parameters




### -param sub






#### - subtractSpan [ref]

Reference to the <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object whose time span is subtracted from the "this" object.


## -returns



When a <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object is returned, it is a new object whose time is the difference between the "this" object and the <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object used as the argument.

When a <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object is returned, it is a new time span object whose value is the difference between the "this" object and the <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object used as an argument.

Any returned objects that has a negative time span or a time before Jan 1, 1601 is set to INVALID_TIME.



