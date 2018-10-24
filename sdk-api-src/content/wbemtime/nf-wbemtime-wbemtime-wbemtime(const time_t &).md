---
UID: NF:wbemtime.WBEMTime.WBEMTime(const time_t &)
title: WBEMTime::WBEMTime(const time_t &)
author: windows-sdk-content
description: The WBEMTime overload class constructor takes an ANSI C time_t structure parameter.
old-location: wmi\wbemtime_wbemtime_const_time_t__.htm
tech.root: WmiSdk
ms.assetid: be698827-c9dc-4f30-9962-2e3f5f2bd029
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: WBEMTime, WBEMTime constructor [Windows Management Instrumentation], WBEMTime constructor [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],WBEMTime constructor, WBEMTime.WBEMTime, WBEMTime.WBEMTime(const time_t &), WBEMTime::WBEMTime, WBEMTime::WBEMTime(const time_t &), WBEMTime::WBEMTime(const time_t&), wbemtime/WBEMTime::WBEMTime, wmi.wbemtime_wbemtime_const_time_t__
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
 - WBEMTime.WBEMTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WBEMTime::WBEMTime(const time_t &)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> overload class constructor takes an ANSI C <b>time_t</b> structure parameter.


## -parameters




### -param t [ref]

ANSI C <b>time_t</b> structure that holds the number of seconds since midnight Jan 1, 1970 (CIM format: 19700101000000.000000-000). For more information, see <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

