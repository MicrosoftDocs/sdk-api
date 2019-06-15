---
UID: NF:evntprov.EventDescGetVersion
title: EventDescGetVersion function (evntprov.h)
author: windows-sdk-content
description: Retrieves the version from the event descriptor.
old-location: etw\eventdescgetversion_func.htm
tech.root: ETW
ms.assetid: 3881f089-d0c6-4d46-929a-09777df13f61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventDescGetVersion, EventDescGetVersion function [ETW], base.eventdescgetversion_func, etw.eventdescgetversion_func, evntprov/EventDescGetVersion
ms.topic: function
f1_keywords: ["evntprov/EventDescGetVersion"]
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
 - EventDescGetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescGetVersion function


## -description


Retrieves
		
		
	
	the version from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the version. See <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>.


## -returns



Version that identifies the revision level of the event definition. 




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>
 

 

