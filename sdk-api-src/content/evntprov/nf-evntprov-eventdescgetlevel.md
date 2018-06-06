---
UID: NF:evntprov.EventDescGetLevel
title: EventDescGetLevel function
author: windows-sdk-content
description: Retrieves the severity level from the event descriptor.
old-location: etw\eventdescgetlevel_func.htm
old-project: ETW
ms.assetid: 29f356ad-c957-4a1e-abf8-5c7e6212c92e
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EventDescGetLevel, EventDescGetLevel function [ETW], base.eventdescgetlevel_func, etw.eventdescgetlevel_func, evntprov/EventDescGetLevel
ms.prod: windows
ms.technology: windows-sdk
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
 - EventDescGetLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescGetLevel function


## -description


Retrieves
		
		
	
	the severity level from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the severity level. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



Severity level that indicates the verboseness with which to log the event.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

