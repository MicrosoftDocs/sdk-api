---
UID: NF:relogger.ITraceEvent.GetEventRecord
title: ITraceEvent::GetEventRecord
author: windows-sdk-content
description: Retrieves the event record that describes an event.
old-location: etw\ievent_geteventrecord.htm
old-project: etw
ms.assetid: 9a1c2313-431a-4243-9272-99dec1bf78dd
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: GetEventRecord, GetEventRecord method [ETW], GetEventRecord method [ETW],ITraceEvent interface, ITraceEvent interface [ETW],GetEventRecord method, ITraceEvent.GetEventRecord, ITraceEvent::GetEventRecord, etw.ievent_geteventrecord, relogger/ITraceEvent::GetEventRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: relogger.h
req.include-header: 
req.redist: 
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
 - ITraceEvent.GetEventRecord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITraceEvent::GetEventRecord


## -description


The <b>GetEventRecord</b> method retrieves the event record that describes an event.


## -parameters




### -param EventRecord [out, retval]

Type: <b><a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">PEVENT_RECORD</a>*</b>

The event record.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Event records describe the metadata associated with an event, such as time logged, length, and the event payload.




## -see-also




<a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/29b6f72a-ae81-4292-a023-a4bab16ae143">ITraceEvent</a>
 

 

