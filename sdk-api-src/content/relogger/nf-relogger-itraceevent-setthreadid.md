---
UID: NF:relogger.ITraceEvent.SetThreadId
title: ITraceEvent::SetThreadId (relogger.h)
description: Sets the identifier of a thread that generates an event.
helpviewer_keywords: ["ITraceEvent interface [ETW]","SetThreadId method","ITraceEvent.SetThreadId","ITraceEvent::SetThreadId","SetThreadId","SetThreadId method [ETW]","SetThreadId method [ETW]","ITraceEvent interface","etw.ievent_setthreadid","relogger/ITraceEvent::SetThreadId"]
old-location: etw\ievent_setthreadid.htm
tech.root: ETW
ms.assetid: 9f5d293e-da87-4b83-9407-fc4179a42a46
ms.date: 12/05/2018
ms.keywords: ITraceEvent interface [ETW],SetThreadId method, ITraceEvent.SetThreadId, ITraceEvent::SetThreadId, SetThreadId, SetThreadId method [ETW], SetThreadId method [ETW],ITraceEvent interface, etw.ievent_setthreadid, relogger/ITraceEvent::SetThreadId
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
 - ITraceEvent::SetThreadId
 - relogger/ITraceEvent::SetThreadId
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
 - ITraceEvent.SetThreadId
---

# ITraceEvent::SetThreadId


## -description

The <b>SetThreadId</b> method sets the identifier of a thread that generates an event.

## -parameters

### -param ThreadId [in]

Type: <b>ULONG</b>

Identifier of the thread that generates the event.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>