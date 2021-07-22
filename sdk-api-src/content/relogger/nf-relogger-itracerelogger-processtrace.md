---
UID: NF:relogger.ITraceRelogger.ProcessTrace
title: ITraceRelogger::ProcessTrace (relogger.h)
description: Delivers events from the associated trace streams to the consumer.
helpviewer_keywords: ["ITraceRelogger interface [ETW]","ProcessTrace method","ITraceRelogger.ProcessTrace","ITraceRelogger::ProcessTrace","ProcessTrace","ProcessTrace method [ETW]","ProcessTrace method [ETW]","ITraceRelogger interface","etw.itracerelogger_processtrace","relogger/ITraceRelogger::ProcessTrace"]
old-location: etw\itracerelogger_processtrace.htm
tech.root: ETW
ms.assetid: ab844b34-0e06-447f-a0b7-dd56ca0b50ed
ms.date: 12/05/2018
ms.keywords: ITraceRelogger interface [ETW],ProcessTrace method, ITraceRelogger.ProcessTrace, ITraceRelogger::ProcessTrace, ProcessTrace, ProcessTrace method [ETW], ProcessTrace method [ETW],ITraceRelogger interface, etw.itracerelogger_processtrace, relogger/ITraceRelogger::ProcessTrace
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
 - ITraceRelogger::ProcessTrace
 - relogger/ITraceRelogger::ProcessTrace
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
 - ITraceRelogger.ProcessTrace
---

# ITraceRelogger::ProcessTrace


## -description

The <b>ProcessTrace</b> method delivers events from the associated trace streams to the consumer.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>
