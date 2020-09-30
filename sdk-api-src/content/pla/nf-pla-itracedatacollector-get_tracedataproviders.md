---
UID: NF:pla.ITraceDataCollector.get_TraceDataProviders
title: ITraceDataCollector::get_TraceDataProviders (pla.h)
description: Retrieves the list of providers enabled for this trace session.
helpviewer_keywords: ["ITraceDataCollector interface [PLA]","TraceDataProviders property","ITraceDataCollector.TraceDataProviders","ITraceDataCollector.get_TraceDataProviders","ITraceDataCollector::TraceDataProviders","ITraceDataCollector::get_TraceDataProviders","TraceDataProviders property [PLA]","TraceDataProviders property [PLA]","ITraceDataCollector interface","base.itracedatacollector_tracedataprovider","get_TraceDataProviders","pla.itracedatacollector_tracedataprovider","pla/ITraceDataCollector::TraceDataProviders","pla/ITraceDataCollector::get_TraceDataProviders"]
old-location: pla\itracedatacollector_tracedataprovider.htm
tech.root: PLA
ms.assetid: 7a2006e8-3c4c-4441-8c9e-be9ce584dd63
ms.date: 12/05/2018
ms.keywords: ITraceDataCollector interface [PLA],TraceDataProviders property, ITraceDataCollector.TraceDataProviders, ITraceDataCollector.get_TraceDataProviders, ITraceDataCollector::TraceDataProviders, ITraceDataCollector::get_TraceDataProviders, TraceDataProviders property [PLA], TraceDataProviders property [PLA],ITraceDataCollector interface, base.itracedatacollector_tracedataprovider, get_TraceDataProviders, pla.itracedatacollector_tracedataprovider, pla/ITraceDataCollector::TraceDataProviders, pla/ITraceDataCollector::get_TraceDataProviders
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITraceDataCollector::get_TraceDataProviders
 - pla/ITraceDataCollector::get_TraceDataProviders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ITraceDataCollector.TraceDataProviders
 - ITraceDataCollector.get_TraceDataProviders
---

# ITraceDataCollector::get_TraceDataProviders


## -description

Retrieves the list of providers enabled for this trace session.

This property is read-only.

## -parameters

## -remarks

If the collection contains a kernel provider, all the providers in the collection must be kernel providers.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>