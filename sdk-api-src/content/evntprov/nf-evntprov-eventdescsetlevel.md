---
UID: NF:evntprov.EventDescSetLevel
title: EventDescSetLevel function
author: windows-driver-content
description: Sets the Level member of the event descriptor.
old-location: etw\eventdescsetlevel_func.htm
old-project: ETW
ms.assetid: a4fe3b0e-6ca5-401c-a669-752e2955cc52
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: EventDescSetLevel, EventDescSetLevel function [ETW], base.eventdescsetlevel_func, etw.eventdescsetlevel_func, evntprov/EventDescSetLevel
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
req.typenames: EVENT_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evntprov.h
api_name:
-	EventDescSetLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescSetLevel function


## -description


Sets the <b>Level</b> member of the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Level [in]

Severity level that indicates the verboseness with which to log the event. For details, see the Level parameter of <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

