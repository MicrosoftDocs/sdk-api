---
UID: NF:pla.ITraceDataCollector.get_ProcessMode
title: ITraceDataCollector::get_ProcessMode (pla.h)
description: Retrieves or sets a value that indicates whether the session is a private, in-process session. (Get)
helpviewer_keywords: ["ITraceDataCollector interface [PLA]","ProcessMode property","ITraceDataCollector.ProcessMode","ITraceDataCollector.get_ProcessMode","ITraceDataCollector::ProcessMode","ITraceDataCollector::get_ProcessMode","ITraceDataCollector::put_ProcessMode","ProcessMode property [PLA]","ProcessMode property [PLA]","ITraceDataCollector interface","base.itracedatacollector_processmode","get_ProcessMode","pla.itracedatacollector_processmode","pla/ITraceDataCollector::ProcessMode","pla/ITraceDataCollector::get_ProcessMode","pla/ITraceDataCollector::put_ProcessMode"]
old-location: pla\itracedatacollector_processmode.htm
tech.root: PLA
ms.assetid: 63962145-7627-46bc-9be1-3a0738bdb1ce
ms.date: 12/05/2018
ms.keywords: ITraceDataCollector interface [PLA],ProcessMode property, ITraceDataCollector.ProcessMode, ITraceDataCollector.get_ProcessMode, ITraceDataCollector::ProcessMode, ITraceDataCollector::get_ProcessMode, ITraceDataCollector::put_ProcessMode, ProcessMode property [PLA], ProcessMode property [PLA],ITraceDataCollector interface, base.itracedatacollector_processmode, get_ProcessMode, pla.itracedatacollector_processmode, pla/ITraceDataCollector::ProcessMode, pla/ITraceDataCollector::get_ProcessMode, pla/ITraceDataCollector::put_ProcessMode
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
 - ITraceDataCollector::get_ProcessMode
 - pla/ITraceDataCollector::get_ProcessMode
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
 - ITraceDataCollector.ProcessMode
 - ITraceDataCollector.get_ProcessMode
 - ITraceDataCollector.put_ProcessMode
---

# ITraceDataCollector::get_ProcessMode


## -description

Retrieves or sets a value that indicates whether the session is a private, in-process session.

This property is read/write.

## -parameters

## -remarks

A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the registered providers that the private session enables and the private session must all be in the same process.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>
