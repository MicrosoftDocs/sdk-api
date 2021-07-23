---
UID: NF:relogger.ITraceRelogger.Inject
title: ITraceRelogger::Inject (relogger.h)
description: Injects a non-system-generated event into the event stream being written to the output trace logfile.
helpviewer_keywords: ["ITraceRelogger interface [ETW]","Inject method","ITraceRelogger.Inject","ITraceRelogger::Inject","Inject","Inject method [ETW]","Inject method [ETW]","ITraceRelogger interface","etw.itracerelogger_inject","relogger/ITraceRelogger::Inject"]
old-location: etw\itracerelogger_inject.htm
tech.root: ETW
ms.assetid: c9d19ad9-182d-469e-b783-2061b7150933
ms.date: 12/05/2018
ms.keywords: ITraceRelogger interface [ETW],Inject method, ITraceRelogger.Inject, ITraceRelogger::Inject, Inject, Inject method [ETW], Inject method [ETW],ITraceRelogger interface, etw.itracerelogger_inject, relogger/ITraceRelogger::Inject
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
 - ITraceRelogger::Inject
 - relogger/ITraceRelogger::Inject
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
 - ITraceRelogger.Inject
---

# ITraceRelogger::Inject


## -description

The <b>Inject</b> method injects a non-system-generated event into the event stream being written to the output trace logfile.

## -parameters

### -param Event [in]

Type: <b>IEvent*</b>

The event to be injected into the stream.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is the primary way to indicate which events should go into the output trace logfile.

To preserve an existing event provided by <a href="/windows/desktop/api/relogger/nf-relogger-itraceeventcallback-onevent">IEventCallback::OnEvent</a>, this method should be called.

## -see-also

<a href="/windows/desktop/api/relogger/nf-relogger-itraceeventcallback-onevent">IEventCallback::OnEvent</a>



<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>