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

# __MIDL___MIDL_itf_eventsys_0000_0009_0001 structure


## -description


Represents a system event structure, which contains the partition and application ID from which an event originated.


## -struct-fields




### -field cbSize

The size of this structure.


### -field changeType

The type of change that has been made to the subscription. For a list of values, see <a href="https://msdn.microsoft.com/99a32590-6875-40ab-997a-c940b25b5de9">EOC_ChangeType</a>.


### -field objectId

The EventClass ID or subscription ID from which the change impacts.


### -field partitionId

The EventClass partition ID or the subscriber partition ID affected.


### -field applicationId

The EventClass application ID or subscriber application ID affected.


### -field reserved

This member is reserved.


## -see-also




<a href="https://msdn.microsoft.com/1b51c7ad-eae7-4030-81c2-ed9259648d31">IEventObjectChange2</a>
 

 

