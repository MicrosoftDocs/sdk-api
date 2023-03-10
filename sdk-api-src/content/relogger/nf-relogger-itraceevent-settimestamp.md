---
UID: NF:relogger.ITraceEvent.SetTimeStamp
title: ITraceEvent::SetTimeStamp (relogger.h)
description: Sets the time at which an event occurred.
helpviewer_keywords: ["ITraceEvent interface [ETW]","SetTimeStamp method","ITraceEvent.SetTimeStamp","ITraceEvent::SetTimeStamp","SetTimeStamp","SetTimeStamp method [ETW]","SetTimeStamp method [ETW]","ITraceEvent interface","etw.ievent_settimestamp","relogger/ITraceEvent::SetTimeStamp"]
old-location: etw\ievent_settimestamp.htm
tech.root: ETW
ms.assetid: e1f76887-8edd-414e-bee3-36b61709c2b5
ms.date: 12/05/2018
ms.keywords: ITraceEvent interface [ETW],SetTimeStamp method, ITraceEvent.SetTimeStamp, ITraceEvent::SetTimeStamp, SetTimeStamp, SetTimeStamp method [ETW], SetTimeStamp method [ETW],ITraceEvent interface, etw.ievent_settimestamp, relogger/ITraceEvent::SetTimeStamp
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
 - ITraceEvent::SetTimeStamp
 - relogger/ITraceEvent::SetTimeStamp
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
 - ITraceEvent.SetTimeStamp
---

# ITraceEvent::SetTimeStamp


## -description

The <b>SetTimeStamp</b> method sets the time at which an event occurred.

## -parameters

### -param TimeStamp [in]

Type: <b>LARGE_INTEGER*</b>

 The time at which the event occurred, in system time.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>