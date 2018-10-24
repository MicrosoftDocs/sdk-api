---
UID: NF:wbemtime.WBEMTime.GetStructtm
title: WBEMTime::GetStructtm
author: windows-sdk-content
description: The GetStructtm method gets the time as an ANSI C run-time struct tm structure.
old-location: wmi\wbemtime_getstructtm.htm
tech.root: WmiSdk
ms.assetid: 569e64c5-1b7e-49ef-abaa-be9b2f85269b
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "?GetStructtm@WBEMTime@@QBEHPAUtm@@@Z, ?GetStructtm@WBEMTime@@QEBAHPEAUtm@@@Z, GetStructtm, GetStructtm method [Windows Management Instrumentation], GetStructtm method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetStructtm method, WBEMTime.GetStructtm, WBEMTime::GetStructtm, _hmm_wbemtime_getstructtm, wbemtime/WBEMTime::GetStructtm, wmi.wbemtime_getstructtm"
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
 - WBEMTime.GetStructtm
 - ?GetStructtm@WBEMTime@@QEBAHPEAUtm@@@Z
 - ?GetStructtm@WBEMTime@@QBEHPAUtm@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTime::GetStructtm


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetStructtm</b> method gets the time as an ANSI C run-time <b>struct tm</b> structure.


## -parameters




### -param ptm

Pointer to an ANSI C run-time <b>struct tm</b> structure.


## -returns



The method returns <b>TRUE</b> if the object's time is equal to or later than midnight Jan 1, 1900.

The method returns <b>FALSE</b> on all other times or if the object's time is set to INVALID_TIME. In this case, the value of <i>ptm</i> is indeterminate.



