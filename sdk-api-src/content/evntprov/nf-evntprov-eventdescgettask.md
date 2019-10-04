---
UID: NF:evntprov.EventDescGetTask
title: EventDescGetTask function (evntprov.h)
author: windows-sdk-content
description: Retrieves the task from the event descriptor.
old-location: etw\eventdescgettask_func.htm
tech.root: ETW
ms.assetid: 5913587d-5c0d-4c50-99d9-8bff266b1c5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventDescGetTask, EventDescGetTask function [ETW], base.eventdescgettask_func, etw.eventdescgettask_func, evntprov/EventDescGetTask
ms.topic: function
f1_keywords:
- evntprov/EventDescGetTask
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
- EventDescGetTask
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescGetTask function


## -description


Retrieves
		
		
	
	the task from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the task. See <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>.


## -returns



Task that identifies the logical component of the application whose events you want to enable.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>
 

 

