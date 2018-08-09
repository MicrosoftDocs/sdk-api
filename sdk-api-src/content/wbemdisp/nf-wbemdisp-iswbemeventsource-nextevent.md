---
UID: NF:wbemdisp.ISWbemEventSource.NextEvent
title: ISWbemEventSource::NextEvent
author: windows-sdk-content
description: If an event is available, the NextEvent method of the SWbemEventSource object retrieves the event from an event query.
old-location: wmi\swbemeventsource_nextevent.htm
old-project: WmiSdk
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemEventSource interface [Windows Management Instrumentation],NextEvent method, ISWbemEventSource.NextEvent, ISWbemEventSource::NextEvent, NextEvent, NextEvent method [Windows Management Instrumentation], NextEvent method [Windows Management Instrumentation],ISWbemEventSource interface, NextEvent method [Windows Management Instrumentation],SWbemEventSource object, SWbemEventSource object [Windows Management Instrumentation],NextEvent method, SWbemEventSource.NextEvent, _hmm_swbemeventsource.nextevent, wmi.swbemeventsource_nextevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemEventSource.NextEvent
 - ISWbemEventSource.NextEvent
 - ISWbemEventSource.NextEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemEventSource::NextEvent


## -description


If an event is available, the 
<b>NextEvent</b> method of the 
<a href="https://msdn.microsoft.com/7efd5e6a-4311-4d20-8b05-e9208eec098a">SWbemEventSource</a> object retrieves the event from an event query.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iTimeoutMs [in, optional]

Number of milliseconds the call waits for an event before returning a time-out error. The default value for this parameter is <b>wbemTimeoutInfinite</b> (-1), which directs the call to wait indefinitely.


### -param objWbemObject






## -returns



If the 
<b>NextEvent</b> method is successful, it returns an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that contains the requested event. If the call times out, the returned object is <b>NULL</b> and an error is raised.



