---
UID: NF:relogger.ITraceRelogger.RegisterCallback
title: ITraceRelogger::RegisterCallback (relogger.h)
author: windows-sdk-content
description: Registers an implementation of IEventCallback with the relogger in order to signal trace activity (starting, stopping, and logging new events).
old-location: etw\itracerelogger_registercallback.htm
tech.root: ETW
ms.assetid: d3c739bd-9285-49ec-b2cf-d607f3d9be0c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITraceRelogger interface [ETW],RegisterCallback method, ITraceRelogger.RegisterCallback, ITraceRelogger::RegisterCallback, RegisterCallback, RegisterCallback method [ETW], RegisterCallback method [ETW],ITraceRelogger interface, etw.itracerelogger_registercallback, relogger/ITraceRelogger::RegisterCallback
ms.topic: method
f1_keywords: 
 - "relogger/ITraceRelogger.RegisterCallback"
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
 - ITraceRelogger.RegisterCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceRelogger::RegisterCallback


## -description


The <b>RegisterCallback</b> method registers an implementation of <a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">IEventCallback</a> with the relogger in order to signal trace activity (starting, stopping, and logging new events).


## -parameters




### -param Callback [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceeventcallback">IEventCallback</a>*</b>

The trace activity information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itracerelogger">ITraceRelogger</a>
 

 

