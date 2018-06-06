---
UID: NF:evntprov.EventDescGetVersion
title: EventDescGetVersion function
author: windows-sdk-content
description: Retrieves the version from the event descriptor.
old-location: etw\eventdescgetversion_func.htm
old-project: ETW
ms.assetid: 3881f089-d0c6-4d46-929a-09777df13f61
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EventDescGetVersion, EventDescGetVersion function [ETW], base.eventdescgetversion_func, etw.eventdescgetversion_func, evntprov/EventDescGetVersion
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
 - EventDescGetVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescGetVersion function


## -description



		Retrieves
		
		
	
	the version from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the version. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



Version that identifies the revision level of the event definition. 




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

