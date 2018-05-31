---
UID: NF:relogger.ITraceRelogger.CreateEventInstance
title: ITraceRelogger::CreateEventInstance
author: windows-sdk-content
description: Generates a new event.
old-location: etw\itracerelogger_createeventinstance.htm
old-project: ETW
ms.assetid: 1a000e38-018d-4077-bf4c-0bfec6cdb676
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CreateEventInstance, CreateEventInstance method [ETW], CreateEventInstance method [ETW],ITraceRelogger interface, ITraceRelogger interface [ETW],CreateEventInstance method, ITraceRelogger.CreateEventInstance, ITraceRelogger::CreateEventInstance, etw.itracerelogger_createeventinstance, relogger/ITraceRelogger::CreateEventInstance
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
req.typenames: RECO_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Relogger.h
api_name:
-	ITraceRelogger.CreateEventInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITraceRelogger::CreateEventInstance


## -description


The <b>CreateEventInstance</b> method generates a new event.


## -parameters




### -param TraceHandle [in]

Type: <b>TRACEHANDLE</b>

The trace from which to create the event.


### -param Flags [in]

Type: <b>ULONG</b>

Indicates whether the event is classic or crimson.


### -param Event [out, retval]

Type: <b><a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>**</b>

The newly generated event.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Event metadata will be pulled from <i>TraceHandle</i> but can be modified by the developer before being logged to a trace.




## -see-also




<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>



<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

