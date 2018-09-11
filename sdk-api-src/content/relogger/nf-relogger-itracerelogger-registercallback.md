---
UID: NF:relogger.ITraceRelogger.RegisterCallback
title: ITraceRelogger::RegisterCallback
author: windows-sdk-content
description: Registers an implementation of IEventCallback with the relogger in order to signal trace activity (starting, stopping, and logging new events).
old-location: etw\itracerelogger_registercallback.htm
tech.root: etw
ms.assetid: d3c739bd-9285-49ec-b2cf-d607f3d9be0c
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: ITraceRelogger interface [ETW],RegisterCallback method, ITraceRelogger.RegisterCallback, ITraceRelogger::RegisterCallback, RegisterCallback, RegisterCallback method [ETW], RegisterCallback method [ETW],ITraceRelogger interface, etw.itracerelogger_registercallback, relogger/ITraceRelogger::RegisterCallback
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
 - ITraceRelogger.RegisterCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceRelogger::RegisterCallback


## -description


The <b>RegisterCallback</b> method registers an implementation of <a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">IEventCallback</a> with the relogger in order to signal trace activity (starting, stopping, and logging new events).


## -parameters




### -param Callback [in]

Type: <b><a href="https://msdn.microsoft.com/70139402-86e6-43b4-9016-42854ef998fd">IEventCallback</a>*</b>

The trace activity information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/08073b9a-5ae0-4e88-a502-647567418005">ITraceRelogger</a>
 

 

