---
UID: NF:relogger.ITraceEvent.GetUserContext
title: ITraceEvent::GetUserContext (relogger.h)
description: Retrieves the user context associated with the stream to which the event belongs.
helpviewer_keywords: ["GetUserContext","GetUserContext method [ETW]","GetUserContext method [ETW]","ITraceEvent interface","ITraceEvent interface [ETW]","GetUserContext method","ITraceEvent.GetUserContext","ITraceEvent::GetUserContext","etw.ievent_getusercontext","relogger/ITraceEvent::GetUserContext"]
old-location: etw\ievent_getusercontext.htm
tech.root: ETW
ms.assetid: 9d4d8abd-b48a-487b-bb73-a6fa48c512c7
ms.date: 12/05/2018
ms.keywords: GetUserContext, GetUserContext method [ETW], GetUserContext method [ETW],ITraceEvent interface, ITraceEvent interface [ETW],GetUserContext method, ITraceEvent.GetUserContext, ITraceEvent::GetUserContext, etw.ievent_getusercontext, relogger/ITraceEvent::GetUserContext
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
 - ITraceEvent::GetUserContext
 - relogger/ITraceEvent::GetUserContext
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
 - ITraceEvent.GetUserContext
---

# ITraceEvent::GetUserContext


## -description

The <b>GetUserContext</b> method retrieves the user context associated with the stream to which the event belongs.

## -parameters

### -param UserContext [out, retval]

Type: <b>void**</b>

The user context. This is the context specified in the call to <a href="/windows/desktop/api/relogger/nf-relogger-itracerelogger-addlogfiletracestream">ITraceRelogger::AddLogfileTraceStream</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>



<a href="/windows/desktop/api/relogger/nf-relogger-itracerelogger-addlogfiletracestream">ITraceRelogger::AddLogfileTraceStream</a>



<a href="/windows/desktop/api/relogger/nf-relogger-itracerelogger-addrealtimetracestream">ITraceRelogger::AddRealtimeTraceStream</a>