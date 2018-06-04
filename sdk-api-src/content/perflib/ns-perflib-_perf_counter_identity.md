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

# _PERF_COUNTER_IDENTITY structure


## -description


Defines the counter that is sent to a provider's callback when the consumer adds or removes a counter from the query.


## -struct-fields




### -field CounterSetGuid

GUID that uniquely identifies the counter set that this counter belongs to.


### -field BufferSize

Size, in bytes, of this structure and the computer name and instance name that are appended to this structure in memory.


### -field CounterId

Unique identifier of the counter in the counter set. 

This member is set to <b>PERF_WILDCARD_COUNTER</b> if the consumer wants to add or remove all counters in the counter set.


### -field InstanceId

Identifier of the counter set instance to which the counter belongs. 

Ignore this value if the instance name at <b>NameOffset</b> is PERF_WILDCARD_INSTANCE.


### -field MachineOffset

Offset to the null-terminated Unicode computer name that follows this structure in memory.


### -field NameOffset

Offset to the null-terminated Unicode instance name that follows this structure in memory.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/0f771ab7-af42-481b-b2da-20dcdf49b82b">ControlCallback</a>
 

 

