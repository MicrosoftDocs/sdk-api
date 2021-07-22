---
UID: NF:relogger.ITraceRelogger.CreateEventInstance
title: ITraceRelogger::CreateEventInstance (relogger.h)
description: Generates a new event.
helpviewer_keywords: ["CreateEventInstance","CreateEventInstance method [ETW]","CreateEventInstance method [ETW]","ITraceRelogger interface","ITraceRelogger interface [ETW]","CreateEventInstance method","ITraceRelogger.CreateEventInstance","ITraceRelogger::CreateEventInstance","etw.itracerelogger_createeventinstance","relogger/ITraceRelogger::CreateEventInstance"]
old-location: etw\itracerelogger_createeventinstance.htm
tech.root: ETW
ms.assetid: 1a000e38-018d-4077-bf4c-0bfec6cdb676
ms.date: 12/05/2018
ms.keywords: CreateEventInstance, CreateEventInstance method [ETW], CreateEventInstance method [ETW],ITraceRelogger interface, ITraceRelogger interface [ETW],CreateEventInstance method, ITraceRelogger.CreateEventInstance, ITraceRelogger::CreateEventInstance, etw.itracerelogger_createeventinstance, relogger/ITraceRelogger::CreateEventInstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceRelogger::CreateEventInstance
 - relogger/ITraceRelogger::CreateEventInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceRelogger.CreateEventInstance
---

# ITraceRelogger::CreateEventInstance


## -description

The <b>CreateEventInstance</b> method generates a new event.

## -parameters

### -param TraceHandle [in]

Type: <b>TRACEHANDLE</b>

The trace from which to create the event.

### -param Flags [in]

Type: <b>ULONG</b>

Indicates whether the event is classic or crimson.

### -param Event [out, retval]

Type: <b><a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>**</b>

The newly generated event.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Event metadata will be pulled from <i>TraceHandle</i> but can be modified by the developer before being logged to a trace.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>



<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>