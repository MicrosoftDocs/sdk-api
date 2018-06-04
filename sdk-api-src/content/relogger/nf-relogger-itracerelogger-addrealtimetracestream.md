---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITraceRelogger::AddRealtimeTraceStream


## -description


The <b>AddRealtimeTraceStream</b> method adds a new real-time ETW trace stream to the relogger. 


## -parameters




### -param LoggerName [in]

Type: <b>BSTR</b>

The real-time logger generating the events to relog


### -param UserContext [in]

Type: <b>void*</b>

The user context under which to relog these events.


### -param TraceHandle [out, retval]

Type: <b>TRACEHANDLE*</b>

Handle to be used when adding new artificial events to the trace stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Events in the newly-added stream will generate callbacks to the <a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">IEventCallback</a> object associated with this relogger.




## -see-also




<a href="https://msdn.microsoft.com/039a9f66-228e-4258-9967-2b2cd7d31091">Consuming Events</a>



<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

