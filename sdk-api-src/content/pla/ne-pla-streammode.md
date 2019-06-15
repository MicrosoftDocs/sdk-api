---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0006
title: StreamMode (pla.h)
author: windows-sdk-content
description: Defines where the trace events are delivered.
old-location: pla\streammode.htm
tech.root: PLA
ms.assetid: 38d9e78f-4ac1-4d65-80e7-9b32c5e79604
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StreamMode, StreamMode enumeration [PLA], base.streammode, pla.streammode, pla/StreamMode, pla/plaBoth, pla/plaBuffering, pla/plaFile, pla/plaRealTime, plaBoth, plaBuffering, plaFile, plaRealTime
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - StreamMode
product: Windows
targetos: Windows
req.typenames: StreamMode
req.redist: 
ms.custom: 19H1
---

# StreamMode enumeration


## -description


Defines where the trace events are delivered.


## -enum-fields




### -field plaFile

Write the trace events to a log file.


### -field plaRealTime

Deliver the trace events to a real time consumer.


### -field plaBoth

Write the trace events to a log file and deliver them to a real-time consumer.


### -field plaBuffering

For details, see the <a href="https://docs.microsoft.com/windows/desktop/ETW/logging-mode-constants">EVENT_TRACE_BUFFERING_MODE</a> logging mode in Event Tracing for Windows.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_streammode">ITraceDataCollector::StreamMode</a>
 

 

