---
UID: NF:evntprov.EventDescGetKeyword
title: EventDescGetKeyword function
author: windows-sdk-content
description: Retrieves the keyword from the event descriptor.
old-location: etw\eventdescgetkeyword_func.htm
old-project: etw
ms.assetid: 4c96fad0-23c4-44cc-8b8f-2d62f08429d2
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: EventDescGetKeyword, EventDescGetKeyword function [ETW], base.eventdescgetkeyword_func, etw.eventdescgetkeyword_func, evntprov/EventDescGetKeyword
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evntprov.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EVENT_INFO_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntprov.h
api_name:
 - EventDescGetKeyword
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescGetKeyword function


## -description


Retrieves
		
		
	
	the keyword from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the keyword. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



Keyword that is a bitmask that further defines the category of events to which the event belongs.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

