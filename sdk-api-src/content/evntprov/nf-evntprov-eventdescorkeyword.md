---
UID: NF:evntprov.EventDescOrKeyword
title: EventDescOrKeyword function (evntprov.h)
author: windows-sdk-content
description: Adds another keyword to the event descriptor.
old-location: etw\eventdescorkeyword_func.htm
tech.root: ETW
ms.assetid: ad5e06cf-e2fa-4696-9521-61ff012b9204
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventDescOrKeyword, EventDescOrKeyword function [ETW], base.eventdescorkeyword_func, etw.eventdescorkeyword_func, evntprov/EventDescOrKeyword
ms.topic: function
f1_keywords: ["evntprov/EventDescOrKeyword"]
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
 - EventDescOrKeyword
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescOrKeyword function


## -description


Adds another keyword to the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>.


### -param Keyword [in]

New keyword to add to the current keyword bitmask.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>
 

 

