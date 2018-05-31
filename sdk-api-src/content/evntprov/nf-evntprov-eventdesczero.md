---
UID: NF:evntprov.EventDescZero
title: EventDescZero function
author: windows-sdk-content
description: Initializes an event descriptor to zero.
old-location: etw\eventdesczero.htm
old-project: ETW
ms.assetid: c52c5f6b-c7ab-47c2-8bce-55323bae7917
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EventDescZero, EventDescZero function [ETW], base.eventdesczero, etw.eventdesczero, evntprov/EventDescZero
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
req.typenames: EVENT_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evntprov.h
api_name:
-	EventDescZero
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescZero function


## -description


Initializes an event descriptor to zero.


## -parameters




### -param EventDescriptor [out]

The event descriptor. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



This function does not return a value.




## -remarks



This is a convenience macro for initializing the memory of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure to zero.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

