---
UID: NF:evntprov.EventDescCreate
title: EventDescCreate function
author: windows-sdk-content
description: Sets the values of an event descriptor.
old-location: etw\eventdesccreate_func.htm
old-project: etw
ms.assetid: 05ce400e-c2e5-4852-9c41-d98ac2a6b467
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: EventDescCreate, EventDescCreate function [ETW], base.eventdesccreate_func, etw.eventdesccreate_func, evntprov/EventDescCreate
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
 - EventDescCreate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescCreate function


## -description



		Sets the values of an event descriptor.
		
		
	
	


## -parameters




### -param EventDescriptor [out]

Event descriptor whose member values are set to those of the remaining parameters. For details, see <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Id [in]

Event identifier. The value is used to set the <b>Id</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Version [in]

Version of the event. The value is used to set the <b>Version</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Channel [in]

The category of events to which this event belongs. The value is used to set the <b>Channel</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Level [in]

Specifies the severity of the event. The value is used to set the <b>Level</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Task [in]

Identifies a logical component of the application whose events you want to enable. The value is used to set the <b>Task</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Opcode [in]

Operation being performed at the time the event was written. The value is used to set the <b>Opcode</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Keyword [in]

Bitmask that further defines the category of events to which the event belongs. The value is used to set the <b>Keyword</b> member of <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


## -returns



This function does not return a value.




## -remarks



This is a convenience macro for setting the members of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c52c5f6b-c7ab-47c2-8bce-55323bae7917">EventDescZero</a>
 

 

