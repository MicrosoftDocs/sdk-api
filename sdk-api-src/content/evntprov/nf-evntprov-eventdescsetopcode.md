---
UID: NF:evntprov.EventDescSetOpcode
title: EventDescSetOpcode function (evntprov.h)
author: windows-sdk-content
description: Sets the Opcode member of the event descriptor.
old-location: etw\eventdescsetopcode_func.htm
tech.root: ETW
ms.assetid: fe16eae0-5bff-4266-9b91-4b714540bde3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventDescSetOpcode, EventDescSetOpcode function [ETW], base.eventdescsetopcode_func, etw.eventdescsetopcode_func, evntprov/EventDescSetOpcode
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
 - EventDescSetOpcode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventDescSetOpcode function


## -description


Sets the <b>Opcode</b> member of the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Opcode [in]

Operation code that identifies the operation being performed at the time the event was written.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

