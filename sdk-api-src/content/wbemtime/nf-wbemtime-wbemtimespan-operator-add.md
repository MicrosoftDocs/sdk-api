---
UID: NF:wbemtime.WBEMTimeSpan.operator-add
title: WBEMTimeSpan::operator-add
author: windows-sdk-content
description: The WBEMTimeSpan class add operator adds one time span to another, placing the sum in a new WBEMTimeSpan object returned by the method.
old-location: wmi\wbemtimespan_operator_plus.htm
tech.root: WmiSdk
ms.assetid: 48e0fcbe-a8a0-4193-b55f-ed4bb7d98614
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WBEMTimeSpan interface [Windows Management Instrumentation],operator+ method, WBEMTimeSpan.operator+, WBEMTimeSpan.operator-add, WBEMTimeSpan::operator+, WBEMTimeSpan::operator-add, _hmm_wbemtimespan_operator_plus, operator+, operator+ method [Windows Management Instrumentation], operator+ method [Windows Management Instrumentation],WBEMTimeSpan interface, wbemtime/WBEMTimeSpan::operator+, wmi.wbemtimespan_operator_plus
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
 - WBEMTimeSpan.operator+
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTimeSpan::operator-add


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa393989(v=VS.85).aspx">WBEMTimeSpan</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>WBEMTimeSpan</b> class add operator adds one time span to another, placing the sum in a new <b>WBEMTimeSpan</b> object returned by the method.


## -parameters




### -param uAdd [ref]

Reference to a <a href="https://msdn.microsoft.com/en-us/library/Aa393989(v=VS.85).aspx">WBEMTimeSpan</a> object, whose time span is added to this one.


## -returns



The method returns a new <a href="https://msdn.microsoft.com/en-us/library/Aa393989(v=VS.85).aspx">WBEMTimeSpan</a> object, whose time span is equal to the sum of its two <b>WBEMTimeSpan</b> arguments.



