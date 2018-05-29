---
UID: NS:evntprov._EVENT_DATA_DESCRIPTOR
title: "_EVENT_DATA_DESCRIPTOR"
author: windows-sdk-content
description: Defines one of the data items of the event data.
old-location: etw\event_data_descriptor.htm
old-project: ETW
ms.assetid: 452ce6f6-3857-4f88-b501-44dd6091b97e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PEVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR structure [ETW], PEVENT_DATA_DESCRIPTOR, PEVENT_DATA_DESCRIPTOR structure pointer [ETW], _EVENT_DATA_DESCRIPTOR, base.event_data_descriptor, etw.event_data_descriptor, evntprov/EVENT_DATA_DESCRIPTOR, evntprov/PEVENT_DATA_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: EVENT_DATA_DESCRIPTOR, *PEVENT_DATA_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evntprov.h
api_name:
-	EVENT_DATA_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EVENT_DATA_DESCRIPTOR structure


## -description


The <b>EVENT_DATA_DESCRIPTOR </b> structure defines one of the data items of the event data.


## -struct-fields




### -field Ptr

A pointer to the data.


### -field Size

The size, in bytes, of the data.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Reserved

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Type

Reserved.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved1

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved2

 




## -remarks



If your event data consists of multiple data items, you would create an array of <b>EVENT_DATA_DESCRIPTOR </b> structures and call the <a href="https://msdn.microsoft.com/a5823ad0-0710-4fd2-9b44-a60a42f138fd">EventDataDescCreate</a> macro to initialize each element with this information. For an example, see <a href="https://msdn.microsoft.com/76e7202e-74ce-40a3-a04b-9af5117fe20e">Writing Manifest-based Events</a>. 

Note that the total data size of the event (not just this data item) is the lesser of 

<ul>
<li>64 KB</li>
</ul>
And

<ul>
<li>The session's buffer size minus the size of the buffer's header (0x48 bytes) minus the sum of the size of the <a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a> structure and each extended data item (the <a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a> structure) that the controller wants to include in the event data.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a>



<a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a>



<a href="https://msdn.microsoft.com/a5823ad0-0710-4fd2-9b44-a60a42f138fd">EventDataDescCreate</a>



<a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a>



<a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a>



<a href="https://msdn.microsoft.com/76e7202e-74ce-40a3-a04b-9af5117fe20e">Writing Manifest-based Events</a>
 

 

