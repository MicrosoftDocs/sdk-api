---
UID: NF:relogger.ITraceEventCallback.OnEvent
title: ITraceEventCallback::OnEvent
author: windows-sdk-content
description: Indicates that an event has been received on the trace streams associated with a relogger.
old-location: etw\ieventcallback_onevent.htm
tech.root: etw
ms.assetid: 2099db80-89fd-4ce1-a7ca-e79abbd7b9e5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ITraceEventCallback interface [ETW],OnEvent method, ITraceEventCallback.OnEvent, ITraceEventCallback::OnEvent, OnEvent, OnEvent method [ETW], OnEvent method [ETW],ITraceEventCallback interface, etw.ieventcallback_onevent, relogger/ITraceEventCallback::OnEvent
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
 - ITraceEventCallback.OnEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceEventCallback::OnEvent


## -description


The <b>OnEvent</b> method indicates that an event has been received on the trace streams associated with a relogger.


## -parameters




### -param Event [in]

Type: <b><a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>*</b>

The event being logged.


### -param Relogger [in]

Type: <b><a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>*</b>

The trace relogger that was used to register this callback and relog this trace.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">ITraceEventCallback</a>
 

 

