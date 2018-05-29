---
UID: NF:relogger.ITraceRelogger.Inject
title: ITraceRelogger::Inject
author: windows-sdk-content
description: Injects a non-system-generated event into the event stream being written to the output trace logfile.
old-location: etw\itracerelogger_inject.htm
old-project: ETW
ms.assetid: c9d19ad9-182d-469e-b783-2061b7150933
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ITraceRelogger interface [ETW],Inject method, ITraceRelogger.Inject, ITraceRelogger::Inject, Inject, Inject method [ETW], Inject method [ETW],ITraceRelogger interface, etw.itracerelogger_inject, relogger/ITraceRelogger::Inject
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
-	ITraceRelogger.Inject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITraceRelogger::Inject


## -description


The <b>Inject</b> method injects a non-system-generated event into the event stream being written to the output trace logfile.


## -parameters




### -param Event [in]

Type: <b>IEvent*</b>

The event to be injected into the stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is the primary way to indicate which events should go into the output trace logfile.

To preserve an existing event provided by <a href="https://msdn.microsoft.com/2099db80-89fd-4ce1-a7ca-e79abbd7b9e5">IEventCallback::OnEvent</a>, this method should be called.




## -see-also




<a href="https://msdn.microsoft.com/2099db80-89fd-4ce1-a7ca-e79abbd7b9e5">IEventCallback::OnEvent</a>



<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

