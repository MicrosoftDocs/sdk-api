---
UID: NF:pla.ITraceDataCollector.put_ProcessMode
title: ITraceDataCollector::put_ProcessMode
author: windows-sdk-content
description: Retrieves or sets a value that indicates whether the session is a private, in-process session.
old-location: pla\itracedatacollector_processmode.htm
tech.root: pla
ms.assetid: 63962145-7627-46bc-9be1-3a0738bdb1ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITraceDataCollector interface [PLA],ProcessMode property, ITraceDataCollector.ProcessMode, ITraceDataCollector.put_ProcessMode, ITraceDataCollector::ProcessMode, ITraceDataCollector::get_ProcessMode, ITraceDataCollector::put_ProcessMode, ProcessMode property [PLA], ProcessMode property [PLA],ITraceDataCollector interface, base.itracedatacollector_processmode, pla.itracedatacollector_processmode, pla/ITraceDataCollector::ProcessMode, pla/ITraceDataCollector::get_ProcessMode, pla/ITraceDataCollector::put_ProcessMode, put_ProcessMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataCollector::put_ProcessMode


## -description


Retrieves or sets a value that indicates whether the session is a private, in-process session.

This property is read/write.


## -parameters


## -remarks



A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the registered providers that the private session enables and the private session must all be in the same process.




## -see-also




<a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a>
 

 

