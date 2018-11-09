---
UID: NF:evntprov.EventDescGetOpcode
title: EventDescGetOpcode function
author: windows-sdk-content
description: Retrieves the operation code from the event descriptor.
old-location: etw\eventdescgetopcode_func.htm
tech.root: etw
ms.assetid: cdca1dd8-da75-408c-9b57-0ac2bfe387b4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EventDescGetOpcode, EventDescGetOpcode function [ETW], base.eventdescgetopcode_func, etw.eventdescgetopcode_func, evntprov/EventDescGetOpcode
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
 - EventDescGetOpcode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EventDescGetOpcode function


## -description


Retrieves
		
		
	
	the operation code from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the operation code. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



Operation code that identifies the operation being performed at the time the event was written.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

