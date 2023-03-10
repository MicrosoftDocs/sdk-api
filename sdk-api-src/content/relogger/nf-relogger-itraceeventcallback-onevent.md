---
UID: NF:relogger.ITraceEventCallback.OnEvent
title: ITraceEventCallback::OnEvent (relogger.h)
description: Indicates that an event has been received on the trace streams associated with a relogger.
helpviewer_keywords: ["ITraceEventCallback interface [ETW]","OnEvent method","ITraceEventCallback.OnEvent","ITraceEventCallback::OnEvent","OnEvent","OnEvent method [ETW]","OnEvent method [ETW]","ITraceEventCallback interface","etw.ieventcallback_onevent","relogger/ITraceEventCallback::OnEvent"]
old-location: etw\ieventcallback_onevent.htm
tech.root: ETW
ms.assetid: 2099db80-89fd-4ce1-a7ca-e79abbd7b9e5
ms.date: 12/05/2018
ms.keywords: ITraceEventCallback interface [ETW],OnEvent method, ITraceEventCallback.OnEvent, ITraceEventCallback::OnEvent, OnEvent, OnEvent method [ETW], OnEvent method [ETW],ITraceEventCallback interface, etw.ieventcallback_onevent, relogger/ITraceEventCallback::OnEvent
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
 - ITraceEventCallback::OnEvent
 - relogger/ITraceEventCallback::OnEvent
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
 - ITraceEventCallback.OnEvent
---

# ITraceEventCallback::OnEvent


## -description

The <b>OnEvent</b> method indicates that an event has been received on the trace streams associated with a relogger.

## -parameters

### -param Event [in]

Type: <b><a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>*</b>

The event being logged.

### -param Relogger [in]

Type: <b><a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>*</b>

The trace relogger that was used to register this callback and relog this trace.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a>