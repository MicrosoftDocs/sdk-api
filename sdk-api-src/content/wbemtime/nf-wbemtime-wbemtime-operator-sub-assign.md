---
UID: NF:wbemtime.WBEMTime.operator-sub-assign
title: WBEMTime::operator-sub-assign (wbemtime.h)
author: windows-sdk-content
description: The WBEMTime class subtract-and-assign (&#8211;=) operator has been overloaded to decrement an object's time by a time span.
old-location: wmi\wbemtime_operator_minus_equal.htm
tech.root: WmiSdk
ms.assetid: 842cfddd-f137-46ba-9744-e3a71dd82f01
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator-= method, WBEMTime.operator-=, WBEMTime.operator-sub-assign, WBEMTime::operator-=, WBEMTime::operator-sub-assign, _hmm_wbemtime_operator_minus_equal, operator-=, operator-= method [Windows Management Instrumentation], operator-= method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator-=, wmi.wbemtime_operator_minus_equal
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
 - WBEMTime.operator-=
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTime::operator-sub-assign


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class subtract-and-assign (–=) operator has been overloaded to decrement an object's time by a time span.


## -parameters




### -param sub [ref]

Reference to the <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object, whose time span is subtracted from the specified object.


## -remarks



The return value is a new <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> object with a value equal to the "this" object after it has been decremented.



