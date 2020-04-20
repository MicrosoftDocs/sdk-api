---
UID: NF:evntprov.EventDescGetOpcode
title: EventDescGetOpcode function (evntprov.h)
description: Retrieves the operation code from the event descriptor.helpviewer_keywords: ["EventDescGetOpcode","EventDescGetOpcode function [ETW]","base.eventdescgetopcode_func","etw.eventdescgetopcode_func","evntprov/EventDescGetOpcode"]
old-location: etw\eventdescgetopcode_func.htm
tech.root: ETW
ms.assetid: cdca1dd8-da75-408c-9b57-0ac2bfe387b4
ms.date: 12/05/2018
ms.keywords: EventDescGetOpcode, EventDescGetOpcode function [ETW], base.eventdescgetopcode_func, etw.eventdescgetopcode_func, evntprov/EventDescGetOpcode
f1_keywords:
- evntprov/EventDescGetOpcode
dev_langs:
- c++
req.header: evntprov.h
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
- Evntprov.h
api_name:
- EventDescGetOpcode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescGetOpcode function


## -description


Retrieves
		
		
	
	the operation code from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the operation code. See <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>.


## -returns



Operation code that identifies the operation being performed at the time the event was written.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>
 

 

