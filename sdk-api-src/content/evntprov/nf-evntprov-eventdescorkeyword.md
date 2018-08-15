---
UID: NF:evntprov.EventDescOrKeyword
title: EventDescOrKeyword function
author: windows-sdk-content
description: Adds another keyword to the event descriptor.
old-location: etw\eventdescorkeyword_func.htm
old-project: ETW
ms.assetid: ad5e06cf-e2fa-4696-9521-61ff012b9204
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EventDescOrKeyword, EventDescOrKeyword function [ETW], base.eventdescorkeyword_func, etw.eventdescorkeyword_func, evntprov/EventDescOrKeyword
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
 - EventDescOrKeyword
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescOrKeyword function


## -description


Adds another keyword to the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Keyword [in]

New keyword to add to the current keyword bitmask.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

