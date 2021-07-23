---
UID: NF:relogger.ITraceEventCallback.OnFinalizeProcessTrace
title: ITraceEventCallback::OnFinalizeProcessTrace (relogger.h)
description: Indicates that a trace is about to end so that relogging can be finalized.
helpviewer_keywords: ["ITraceEventCallback interface [ETW]","OnFinalizeProcessTrace method","ITraceEventCallback.OnFinalizeProcessTrace","ITraceEventCallback::OnFinalizeProcessTrace","OnFinalizeProcessTrace","OnFinalizeProcessTrace method [ETW]","OnFinalizeProcessTrace method [ETW]","ITraceEventCallback interface","etw.ieventcallback_onfinalizeprocesstrace","relogger/ITraceEventCallback::OnFinalizeProcessTrace"]
old-location: etw\ieventcallback_onfinalizeprocesstrace.htm
tech.root: ETW
ms.assetid: b152b6fd-4af5-4781-9c88-c71364ef86ff
ms.date: 12/05/2018
ms.keywords: ITraceEventCallback interface [ETW],OnFinalizeProcessTrace method, ITraceEventCallback.OnFinalizeProcessTrace, ITraceEventCallback::OnFinalizeProcessTrace, OnFinalizeProcessTrace, OnFinalizeProcessTrace method [ETW], OnFinalizeProcessTrace method [ETW],ITraceEventCallback interface, etw.ieventcallback_onfinalizeprocesstrace, relogger/ITraceEventCallback::OnFinalizeProcessTrace
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
 - ITraceEventCallback::OnFinalizeProcessTrace
 - relogger/ITraceEventCallback::OnFinalizeProcessTrace
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
 - ITraceEventCallback.OnFinalizeProcessTrace
---

# ITraceEventCallback::OnFinalizeProcessTrace


## -description

The <b>OnFinalizeProcessTrace</b> trace method indicates that a trace is about to end so that relogging can be finalized.

## -parameters

### -param Relogger [in]

Type: <b><a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>*</b>

The trace relogger that was used to register this callback and relog this trace.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a>