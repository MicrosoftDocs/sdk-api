---
UID: NF:relogger.ITraceEvent.SetProcessId
title: ITraceEvent::SetProcessId (relogger.h)
description: Assigns an event to a specific process.
helpviewer_keywords: ["ITraceEvent interface [ETW]","SetProcessId method","ITraceEvent.SetProcessId","ITraceEvent::SetProcessId","SetProcessId","SetProcessId method [ETW]","SetProcessId method [ETW]","ITraceEvent interface","etw.ievent_setprocessid","relogger/ITraceEvent::SetProcessId"]
old-location: etw\ievent_setprocessid.htm
tech.root: ETW
ms.assetid: c2e5e6bf-cdff-42fa-9352-2f234f39849d
ms.date: 12/05/2018
ms.keywords: ITraceEvent interface [ETW],SetProcessId method, ITraceEvent.SetProcessId, ITraceEvent::SetProcessId, SetProcessId, SetProcessId method [ETW], SetProcessId method [ETW],ITraceEvent interface, etw.ievent_setprocessid, relogger/ITraceEvent::SetProcessId
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
 - ITraceEvent::SetProcessId
 - relogger/ITraceEvent::SetProcessId
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
 - ITraceEvent.SetProcessId
---

# ITraceEvent::SetProcessId


## -description

The <b>SetProcessId</b> method assigns an event to a specific process.

## -parameters

### -param ProcessId [in]

Type: <b>ULONG</b>

Identifier of the process that should own this event.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>