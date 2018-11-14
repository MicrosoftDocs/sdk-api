---
UID: NF:instance.CInstance.SetTimeSpan
title: CInstance::SetTimeSpan
author: windows-sdk-content
description: The SetTimeSpan method sets a property that represents a time span.
old-location: wmi\cinstance_settimespan.htm
tech.root: WmiSdk
ms.assetid: d23197a2-7352-44e8-b962-2509fdf9673d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetTimeSpan method, CInstance.SetTimeSpan, CInstance::SetTimeSpan, SetTimeSpan, SetTimeSpan method [Windows Management Instrumentation], SetTimeSpan method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_settimespan, instance/CInstance::SetTimeSpan, wmi.cinstance_settimespan
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: instance.h
req.include-header: FwCommon.h
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
req.lib: FrameDyn.lib
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
 - CInstance.SetTimeSpan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- instance.h
: 
- CInstance.SetTimeSpan
: 
---

# CInstance::SetTimeSpan


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetTimeSpan</b> method sets a property that represents a time span.


## -parameters




### -param name

Name of the property that is set.


### -param wbemtimespan [ref]

Value assigned to the time span property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not a time span value. More information is available in the log file, Framework.log.



