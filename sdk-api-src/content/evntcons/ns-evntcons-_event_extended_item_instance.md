---
UID: NS:evntcons._EVENT_EXTENDED_ITEM_INSTANCE
title: "_EVENT_EXTENDED_ITEM_INSTANCE"
author: windows-sdk-content
description: Defines the relationship between events if TraceEventInstance was used to log related events.
old-location: etw\event_extended_item_instance.htm
tech.root: etw
ms.assetid: 3def638b-cab2-4b5d-b409-7285caa77ae1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PEVENT_EXTENDED_ITEM_INSTANCE, EVENT_EXTENDED_ITEM_INSTANCE, EVENT_EXTENDED_ITEM_INSTANCE structure [ETW], PEVENT_EXTENDED_ITEM_INSTANCE, PEVENT_EXTENDED_ITEM_INSTANCE structure pointer [ETW], _EVENT_EXTENDED_ITEM_INSTANCE, base.event_extended_item_instance, etw.event_extended_item_instance, evntcons/EVENT_EXTENDED_ITEM_INSTANCE, evntcons/PEVENT_EXTENDED_ITEM_INSTANCE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: evntcons.h
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
 - Evntcons.h
api_name:
 - EVENT_EXTENDED_ITEM_INSTANCE
product: Windows
targetos: Windows
req.typenames: EVENT_EXTENDED_ITEM_INSTANCE, *PEVENT_EXTENDED_ITEM_INSTANCE
req.redist: 
---

# _EVENT_EXTENDED_ITEM_INSTANCE structure


## -description


The <b>EVENT_EXTENDED_ITEM_INSTANCE</b> structure defines the relationship between events if <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> was used to log related events.


## -struct-fields




### -field InstanceId

A unique transaction identifier that maps an event to a specific transaction.


### -field ParentInstanceId

A unique transaction identifier of a parent event if you are mapping a hierarchical relationship.


### -field ParentGuid

A GUID that uniquely identifies the provider that logged the event referenced by the <b>ParentInstanceId</b> member.


## -see-also




<a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">EVENT_HEADER_EXTENDED_DATA_ITEM</a>
 

 

