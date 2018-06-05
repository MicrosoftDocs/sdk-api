---
UID: NF:wbemtime.WBEMTimeSpan.operator-=
title: WBEMTimeSpan::operator-=
author: windows-sdk-content
description: Compares two WBEMTimeSpan objects using the subtract and assign operator (&#8211;=).
old-location: wmi\wbemtimespan_operator_minus_equal.htm
old-project: WmiSdk
ms.assetid: 4cf466bc-278e-4352-a818-ed74ff65903a
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator-= method, WBEMTimeSpan.operator-=, WBEMTimeSpan::operator-=, _hmm_wbemtimespan_operator_minus_equal, operator-=, operator-= method [Windows Management Instrumentation], operator-= method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator-=, wmi.wbemtimespan_operator_minus_equal
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	WBEMTimeSpan.operator-=
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTimeSpan::operator-=


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

Compares two <b>WBEMTimeSpan</b> objects using the subtract and assign operator (–=).


## -parameters




### -param uSub [ref]

Reference to the <b>WBEMTimeSpan</b> object, whose time span is subtracted from the "this" object.


## -returns



This method returns a new <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object with a value equal to the difference in time.



