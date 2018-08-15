---
UID: NF:wbemtime.WBEMTime.GetTime
title: WBEMTime::GetTime
author: windows-sdk-content
description: The GetTime method returns the time as a 64-bit integer.
old-location: wmi\wbemtime_gettime.htm
old-project: WmiSdk
ms.assetid: 1690d33d-c39b-448e-889e-48dce1933fc1
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GetTime, GetTime method [Windows Management Instrumentation], GetTime method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetTime method, WBEMTime.GetTime, WBEMTime::GetTime, _hmm_wbemtime_gettime, wbemtime/WBEMTime::GetTime, wmi.wbemtime_gettime
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
 - WBEMTime.GetTime
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::GetTime


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetTime</b> method returns the time as a 64-bit integer.


## -parameters






## -returns



Returns the time as a GMT <b>FILETIME</b> structure. If the time is invalid, it returns INVALID_TIME.




## -remarks



The method is provided to assist users in debugging.



