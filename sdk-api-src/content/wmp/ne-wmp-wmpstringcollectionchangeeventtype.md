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

# WMPStringCollectionChangeEventType enumeration


## -description



The <b>WMPStringCollectionChangeEventType</b> enumeration type defines the types of changes that can occur in a string collection.



<b>Syntax</b>


## -enum-fields




### -field wmpsccetUnknown

Not a valid event type.


### -field wmpsccetInsert

An item was inserted.


### -field wmpsccetChange

The string collection changed.


### -field wmpsccetDelete

An item was deleted.


### -field wmpsccetClear

The string collection was cleared.


### -field wmpsccetBeginUpdates

Bulk updates are beginning.


### -field wmpsccetEndUpdates

Bulk updates have ended.


## -remarks




          Windows Media Player 10 Mobile: This enumeration is not supported.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/93880116-e354-49d0-ba02-391fbb4d3f8c">IWMPEvents3::StringCollectionChange</a>



<a href="https://msdn.microsoft.com/8cdabea9-7e37-4e63-9d6c-b6f63aa536ea">IWMPStringCollection Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

