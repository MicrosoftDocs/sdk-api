---
UID: NF:wbemtime.WBEMTime.operator+=
title: WBEMTime::operator+=
author: windows-sdk-content
description: The WBEMTime class add-and-assign (+=) operator has been overloaded to increment an object's time by a time span.
old-location: wmi\wbemtime_operator_plus_equal.htm
old-project: WmiSdk
ms.assetid: fedfce44-1da2-4443-8634-e341ffae999a
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: WBEMTime interface [Windows Management Instrumentation],operator+= method, WBEMTime.operator+=, WBEMTime::operator+=, _hmm_wbemtime_operator_plus_equal, operator+=, operator+= method [Windows Management Instrumentation], operator+= method [Windows Management Instrumentation],WBEMTime interface, wbemtime/WBEMTime::operator+=, wmi.wbemtime_operator_plus_equal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemtime.h
req.include-header: 
req.redist: 
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
 - WBEMTime.operator+=
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::operator+=


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

