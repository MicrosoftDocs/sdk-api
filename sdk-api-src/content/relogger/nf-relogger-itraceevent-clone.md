---
UID: NF:relogger.ITraceEvent.Clone
title: ITraceEvent::Clone (relogger.h)
description: Creates a duplicate copy of an event.
helpviewer_keywords: ["Clone","Clone method [ETW]","Clone method [ETW]","ITraceEvent interface","ITraceEvent interface [ETW]","Clone method","ITraceEvent.Clone","ITraceEvent::Clone","etw.ievent_clone","relogger/ITraceEvent::Clone"]
old-location: etw\ievent_clone.htm
tech.root: ETW
ms.assetid: a4fa29f4-a265-4b42-a499-bc53566dc889
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [ETW], Clone method [ETW],ITraceEvent interface, ITraceEvent interface [ETW],Clone method, ITraceEvent.Clone, ITraceEvent::Clone, etw.ievent_clone, relogger/ITraceEvent::Clone
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
 - ITraceEvent::Clone
 - relogger/ITraceEvent::Clone
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
 - ITraceEvent.Clone
---

# ITraceEvent::Clone


## -description

The <b>Clone</b> method creates a duplicate copy of an event.

## -parameters

### -param NewEvent [out, retval]

Type: <b>IEvent**</b>

The new event.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>