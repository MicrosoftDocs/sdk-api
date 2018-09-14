---
UID: NF:relogger.ITraceRelogger.AddRealtimeTraceStream
title: ITraceRelogger::AddRealtimeTraceStream
author: windows-sdk-content
description: Adds a new real-time ETW trace stream to the relogger.
old-location: etw\itracerelogger_addrealtimetracestream.htm
tech.root: ETW
ms.assetid: 68bb5715-49b8-45bc-ae98-0b4a519c8e62
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddRealtimeTraceStream, AddRealtimeTraceStream method [ETW], AddRealtimeTraceStream method [ETW],ITraceRelogger interface, ITraceRelogger interface [ETW],AddRealtimeTraceStream method, ITraceRelogger.AddRealtimeTraceStream, ITraceRelogger::AddRealtimeTraceStream, etw.itracerelogger_addrealtimetracestream, relogger/ITraceRelogger::AddRealtimeTraceStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: relogger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceRelogger.AddRealtimeTraceStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

