---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

