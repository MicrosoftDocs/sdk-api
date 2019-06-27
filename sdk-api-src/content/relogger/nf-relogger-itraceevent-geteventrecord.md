---
UID: NF:relogger.ITraceEvent.GetEventRecord
title: ITraceEvent::GetEventRecord (relogger.h)
author: windows-sdk-content
description: Retrieves the event record that describes an event.
old-location: etw\ievent_geteventrecord.htm
tech.root: ETW
ms.assetid: 9a1c2313-431a-4243-9272-99dec1bf78dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEventRecord, GetEventRecord method [ETW], GetEventRecord method [ETW],ITraceEvent interface, ITraceEvent interface [ETW],GetEventRecord method, ITraceEvent.GetEventRecord, ITraceEvent::GetEventRecord, etw.ievent_geteventrecord, relogger/ITraceEvent::GetEventRecord
ms.topic: method
f1_keywords: 
 - "relogger/ITraceEvent.GetEventRecord"
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
 - ITraceEvent.GetEventRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceEvent::GetEventRecord


## -description


The <b>GetEventRecord</b> method retrieves the event record that describes an event.


## -parameters




### -param EventRecord [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-_event_record">PEVENT_RECORD</a>*</b>

The event record.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 Event records describe the metadata associated with an event, such as time logged, length, and the event payload.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-_event_record">EVENT_RECORD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/relogger/nn-relogger-itraceevent">ITraceEvent</a>
 

 

