---
UID: NF:evntprov.EventDescSetTask
title: EventDescSetTask function (evntprov.h)
description: Sets the Task member of the event descriptor.helpviewer_keywords: ["EventDescSetTask","EventDescSetTask function [ETW]","base.eventdescsettask_func","etw.eventdescsettask_func","evntprov/EventDescSetTask"]
old-location: etw\eventdescsettask_func.htm
tech.root: ETW
ms.assetid: 74298e6f-b29a-4fa7-98d1-f81270fcbc0e
ms.date: 12/05/2018
ms.keywords: EventDescSetTask, EventDescSetTask function [ETW], base.eventdescsettask_func, etw.eventdescsettask_func, evntprov/EventDescSetTask
f1_keywords:
- evntprov/EventDescSetTask
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
- EventDescSetTask
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescSetTask function


## -description


Sets the <b>Task</b> member of the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>.


### -param Task [in]

Task that identifies the logical component of the application whose events you want to enable.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>
 

 

