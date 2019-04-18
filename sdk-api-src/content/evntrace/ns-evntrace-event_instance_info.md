---
UID: NS:evntrace.EVENT_INSTANCE_INFO
title: EVENT_INSTANCE_INFO (evntrace.h)
author: windows-sdk-content
description: The EVENT_INSTANCE_INFO structure maps a unique transaction identifier to a registered event trace class.
old-location: etw\event_instance_info.htm
tech.root: ETW
ms.assetid: 83a3802c-b992-43a2-a98a-bdee2ecfef24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEVENT_INSTANCE_INFO, EVENT_INSTANCE_INFO, EVENT_INSTANCE_INFO structure [ETW], PEVENT_INSTANCE_INFO, PEVENT_INSTANCE_INFO structure pointer [ETW], _evt_event_instance_info, base.event_instance_info, etw.event_instance_info, evntrace/EVENT_INSTANCE_INFO, evntrace/PEVENT_INSTANCE_INFO"
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Evntrace.h
api_name:
 - EVENT_INSTANCE_INFO
product: Windows
targetos: Windows
req.typenames: EVENT_INSTANCE_INFO, *PEVENT_INSTANCE_INFO
req.redist: 
ms.custom: 19H1
---

# EVENT_INSTANCE_INFO structure


## -description


The 
<b>EVENT_INSTANCE_INFO</b> structure maps a unique transaction identifier to a registered event trace class.


## -struct-fields




### -field RegHandle

Handle to a registered event trace class.


### -field InstanceId

Unique transaction identifier that maps an event to a specific transaction.


## -remarks



Be sure to initialize the memory for this structure to zero before setting any members.




## -see-also




<a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a>



<a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a>
 

 

