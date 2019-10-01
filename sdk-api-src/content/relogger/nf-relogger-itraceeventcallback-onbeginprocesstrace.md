---
UID: NF:relogger.ITraceEventCallback.OnBeginProcessTrace
title: ITraceEventCallback::OnBeginProcessTrace (relogger.h)
author: windows-sdk-content
description: Indicates that a trace is about to begin so that relogging can be started.
old-location: etw\ieventcallback_onbeginprocesstrace.htm
tech.root: ETW
ms.assetid: acc6b1c4-9be1-490d-8b82-7ae8e73bd929
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITraceEventCallback interface [ETW],OnBeginProcessTrace method, ITraceEventCallback.OnBeginProcessTrace, ITraceEventCallback::OnBeginProcessTrace, OnBeginProcessTrace, OnBeginProcessTrace method [ETW], OnBeginProcessTrace method [ETW],ITraceEventCallback interface, etw.ieventcallback_onbeginprocesstrace, relogger/ITraceEventCallback::OnBeginProcessTrace
ms.topic: method
f1_keywords: 
 - "relogger/ITraceEventCallback.OnBeginProcessTrace"
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
 - ITraceEventCallback.OnBeginProcessTrace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceEventCallback::OnBeginProcessTrace


## -description


The <b>OnBeginProcessTrace</b> trace method indicates that a trace is about to begin so that relogging can be started.


## -parameters




### -param HeaderEvent [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>*</b>

Supplies a pointer to the header event.


### -param Relogger [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>*</b>

Supplies a pointer to the <b>ITraceRelogger</b> interface, which exposes
        APIs for actual event injection, synthesizing new events, and cloning
        existing events.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">ITraceEventCallback</a>
 

 

