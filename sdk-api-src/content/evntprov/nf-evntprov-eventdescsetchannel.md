---
UID: NF:evntprov.EventDescSetChannel
title: EventDescSetChannel function
author: windows-sdk-content
description: Sets the Channel member of the event descriptor.
old-location: etw\eventdescsetchannel_func.htm
tech.root: etw
ms.assetid: 3580935d-ab7e-4409-b4ac-58f3c6019514
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: EventDescSetChannel, EventDescSetChannel function [ETW], base.eventdescsetchannel_func, etw.eventdescsetchannel_func, evntprov/EventDescSetChannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - EventDescSetChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EventDescSetChannel function


## -description


Sets the <b>Channel</b> member of the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Channel [in]

Channel that defines the category of events to which this event belongs.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

