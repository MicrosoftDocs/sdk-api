---
UID: NF:relogger.ITraceEvent.SetEventDescriptor
title: ITraceEvent::SetEventDescriptor (relogger.h)
description: Sets the event descriptor for an event.
helpviewer_keywords: ["ITraceEvent interface [ETW]","SetEventDescriptor method","ITraceEvent.SetEventDescriptor","ITraceEvent::SetEventDescriptor","SetEventDescriptor","SetEventDescriptor method [ETW]","SetEventDescriptor method [ETW]","ITraceEvent interface","etw.ievent_seteventdescriptor","relogger/ITraceEvent::SetEventDescriptor"]
old-location: etw\ievent_seteventdescriptor.htm
tech.root: ETW
ms.assetid: 729a887e-1759-44d5-a7d5-8385d648eebf
ms.date: 12/05/2018
ms.keywords: ITraceEvent interface [ETW],SetEventDescriptor method, ITraceEvent.SetEventDescriptor, ITraceEvent::SetEventDescriptor, SetEventDescriptor, SetEventDescriptor method [ETW], SetEventDescriptor method [ETW],ITraceEvent interface, etw.ievent_seteventdescriptor, relogger/ITraceEvent::SetEventDescriptor
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
 - ITraceEvent::SetEventDescriptor
 - relogger/ITraceEvent::SetEventDescriptor
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
 - ITraceEvent.SetEventDescriptor
---

# ITraceEvent::SetEventDescriptor


## -description

The <b>SetEventDescriptor</b> method sets the event descriptor for an event.

## -parameters

### -param EventDescriptor [in]

Type: <b><a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">PCEVENT_DESCRIPTOR</a></b>

The event descriptor data.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>