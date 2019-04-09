---
UID: NF:wbemtime.WBEMTime.operator-add-assign
title: WBEMTime::operator-add-assign (wbemtime.h)
author: windows-sdk-content
description: The WBEMTime class add-and-assign (+=) operator has been overloaded to increment an object's time by a time span.
old-location: wmi\wbemtime_operator_plus_equal.htm
tech.root: WmiSdk
ms.assetid: fedfce44-1da2-4443-8634-e341ffae999a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator+= method, WBEMTime.operator+=, WBEMTime.operator-add-assign, WBEMTime::operator+=, WBEMTime::operator-add-assign, _hmm_wbemtime_operator_plus_equal, operator+=, operator+= method [Windows Management Instrumentation], operator+= method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator+=, wmi.wbemtime_operator_plus_equal
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
 - WBEMTime.operator+=
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTime::operator-add-assign


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class add-and-assign (+=) operator has been overloaded to increment an object's time by a time span.


## -parameters




### -param ts [ref]

Reference to the <a href="https://msdn.microsoft.com/bcec87c1-32ba-451b-92bb-80c8a5007adb">WBEMTimeSpan</a> object, whose time is added to the specified object.

