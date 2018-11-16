---
UID: NF:evntprov.EventDescZero
title: EventDescZero function
author: windows-sdk-content
description: Initializes an event descriptor to zero.
old-location: etw\eventdesczero.htm
tech.root: ETW
ms.assetid: c52c5f6b-c7ab-47c2-8bce-55323bae7917
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EventDescZero, EventDescZero function [ETW], base.eventdesczero, etw.eventdesczero, evntprov/EventDescZero
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
 - EventDescZero
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EventDescZero
: 
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
 

 

