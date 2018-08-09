---
UID: NF:relogger.ITraceEventCallback.OnBeginProcessTrace
title: ITraceEventCallback::OnBeginProcessTrace
author: windows-sdk-content
description: Indicates that a trace is about to begin so that relogging can be started.
old-location: etw\ieventcallback_onbeginprocesstrace.htm
old-project: ETW
ms.assetid: acc6b1c4-9be1-490d-8b82-7ae8e73bd929
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ITraceEventCallback interface [ETW],OnBeginProcessTrace method, ITraceEventCallback.OnBeginProcessTrace, ITraceEventCallback::OnBeginProcessTrace, OnBeginProcessTrace, OnBeginProcessTrace method [ETW], OnBeginProcessTrace method [ETW],ITraceEventCallback interface, etw.ieventcallback_onbeginprocesstrace, relogger/ITraceEventCallback::OnBeginProcessTrace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: RECO_RANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceEventCallback.OnBeginProcessTrace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITraceEventCallback::OnBeginProcessTrace


## -description


The <b>OnBeginProcessTrace</b> trace method indicates that a trace is about to begin so that relogging can be started.


## -parameters




### -param HeaderEvent [in]

Type: <b><a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>*</b>

Supplies a pointer to the header event.


### -param Relogger [in]

Type: <b><a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>*</b>

Supplies a pointer to the <b>ITraceRelogger</b> interface, which exposes
        APIs for actual event injection, synthesizing new events, and cloning
        existing events.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">ITraceEventCallback</a>
 

 

