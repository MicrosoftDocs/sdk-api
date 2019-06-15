---
UID: NF:evntprov.EventDescGetChannel
title: EventDescGetChannel function (evntprov.h)
author: windows-sdk-content
description: Retrieves the channel from the event descriptor.
old-location: etw\eventdescgetchannel_func.htm
tech.root: ETW
ms.assetid: 193786ad-751e-477d-8747-a38b43292648
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventDescGetChannel, EventDescGetChannel function [ETW], base.eventdescgetchannel_func, etw.eventdescgetchannel_func, evntprov/EventDescGetChannel
ms.topic: function
f1_keywords: ["evntprov/EventDescGetChannel"]
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
 - EventDescGetChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescGetChannel function


## -description


Retrieves
		
		
	
	the channel from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the channel. See <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>.


## -returns



Channel that defines the category of events to which this event belongs.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>
 

 

