---
UID: NF:relogger.ITraceEventCallback.OnFinalizeProcessTrace
title: ITraceEventCallback::OnFinalizeProcessTrace
author: windows-sdk-content
description: Indicates that a trace is about to end so that relogging can be finalized.
old-location: etw\ieventcallback_onfinalizeprocesstrace.htm
tech.root: etw
ms.assetid: b152b6fd-4af5-4781-9c88-c71364ef86ff
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITraceEventCallback interface [ETW],OnFinalizeProcessTrace method, ITraceEventCallback.OnFinalizeProcessTrace, ITraceEventCallback::OnFinalizeProcessTrace, OnFinalizeProcessTrace, OnFinalizeProcessTrace method [ETW], OnFinalizeProcessTrace method [ETW],ITraceEventCallback interface, etw.ieventcallback_onfinalizeprocesstrace, relogger/ITraceEventCallback::OnFinalizeProcessTrace
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Relogger.h
api_name:
 - ITraceEventCallback.OnFinalizeProcessTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- relogger.h
: 
- ITraceEventCallback.OnFinalizeProcessTrace
: 
---

# ITraceEventCallback::OnFinalizeProcessTrace


## -description


The <b>OnFinalizeProcessTrace</b> trace method indicates that a trace is about to end so that relogging can be finalized.


## -parameters




### -param Relogger [in]

Type: <b><a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>*</b>

The trace relogger that was used to register this callback and relog this trace.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">ITraceEventCallback</a>
 

 

