---
UID: NF:relogger.ITraceRelogger.RegisterCallback
title: ITraceRelogger::RegisterCallback (relogger.h)
description: Registers an implementation of IEventCallback with the relogger in order to signal trace activity (starting, stopping, and logging new events).
helpviewer_keywords: ["ITraceRelogger interface [ETW]","RegisterCallback method","ITraceRelogger.RegisterCallback","ITraceRelogger::RegisterCallback","RegisterCallback","RegisterCallback method [ETW]","RegisterCallback method [ETW]","ITraceRelogger interface","etw.itracerelogger_registercallback","relogger/ITraceRelogger::RegisterCallback"]
old-location: etw\itracerelogger_registercallback.htm
tech.root: ETW
ms.assetid: d3c739bd-9285-49ec-b2cf-d607f3d9be0c
ms.date: 12/05/2018
ms.keywords: ITraceRelogger interface [ETW],RegisterCallback method, ITraceRelogger.RegisterCallback, ITraceRelogger::RegisterCallback, RegisterCallback, RegisterCallback method [ETW], RegisterCallback method [ETW],ITraceRelogger interface, etw.itracerelogger_registercallback, relogger/ITraceRelogger::RegisterCallback
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
 - ITraceRelogger::RegisterCallback
 - relogger/ITraceRelogger::RegisterCallback
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
 - ITraceRelogger.RegisterCallback
---

# ITraceRelogger::RegisterCallback


## -description

The <b>RegisterCallback</b> method registers an implementation of <a href="/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">IEventCallback</a> with the relogger in order to signal trace activity (starting, stopping, and logging new events).

## -parameters

### -param Callback [in]

Type: <b><a href="/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">IEventCallback</a>*</b>

The trace activity information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>