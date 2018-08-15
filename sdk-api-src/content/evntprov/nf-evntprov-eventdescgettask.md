---
UID: NF:evntprov.EventDescGetTask
title: EventDescGetTask function
author: windows-sdk-content
description: Retrieves the task from the event descriptor.
old-location: etw\eventdescgettask_func.htm
old-project: ETW
ms.assetid: 5913587d-5c0d-4c50-99d9-8bff266b1c5b
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EventDescGetTask, EventDescGetTask function [ETW], base.eventdescgettask_func, etw.eventdescgettask_func, evntprov/EventDescGetTask
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
 - EventDescGetTask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescGetTask function


## -description


Retrieves
		
		
	
	the task from the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor from which to retrieve the task. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



Task that identifies the logical component of the application whose events you want to enable.




## -remarks



This is a convenience macro for retrieving the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

