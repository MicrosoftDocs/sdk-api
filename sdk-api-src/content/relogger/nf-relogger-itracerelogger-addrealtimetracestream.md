---
UID: NF:relogger.ITraceRelogger.AddRealtimeTraceStream
title: ITraceRelogger::AddRealtimeTraceStream (relogger.h)
description: Adds a new real-time ETW trace stream to the relogger.
old-location: etw\itracerelogger_addrealtimetracestream.htm
tech.root: ETW
ms.assetid: 68bb5715-49b8-45bc-ae98-0b4a519c8e62
ms.date: 12/05/2018
ms.keywords: AddRealtimeTraceStream, AddRealtimeTraceStream method [ETW], AddRealtimeTraceStream method [ETW],ITraceRelogger interface, ITraceRelogger interface [ETW],AddRealtimeTraceStream method, ITraceRelogger.AddRealtimeTraceStream, ITraceRelogger::AddRealtimeTraceStream, etw.itracerelogger_addrealtimetracestream, relogger/ITraceRelogger::AddRealtimeTraceStream
ms.topic: method
f1_keywords:
- relogger/ITraceRelogger.AddRealtimeTraceStream
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Events in the newly-added stream will generate callbacks to the <a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">IEventCallback</a> object associated with this relogger.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/consuming-events">Consuming Events</a>



<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>
 

 

