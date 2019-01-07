---
UID: NF:evntprov.EventDescGetId
title: EventDescGetId function
author: windows-sdk-content
description: Retrieves the event identifier from the event descriptor.
old-location: etw\eventdescgetid_func.htm
tech.root: ETW
ms.assetid: 33deea6e-27e0-44ae-8d18-e8c854bc1819
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EventDescGetId, EventDescGetId function [ETW], base.eventdescgetid_func, etw.eventdescgetid_func, evntprov/EventDescGetId
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
 - EventDescGetId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EventDescGetId function


## -description


Retrieves
		
		
	
	the event identifier from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the event identifier. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



The event identifier.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

