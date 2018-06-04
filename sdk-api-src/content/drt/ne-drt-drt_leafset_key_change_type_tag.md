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

# drt_leafset_key_change_type_tag enumeration


## -description


The <b>DRT_LEAFSET_KEY_CHANGE_TYPE</b> enumeration defines  the set of   changes that can occur on nodes in the leaf set of a locally registered key.


## -enum-fields




### -field DRT_LEAFSET_KEY_ADDED

A node was added to the  DRT leaf set of the local node.


### -field DRT_LEAFSET_KEY_DELETED

A node was deleted from the  DRT leaf set of the local node.


## -remarks



This enumeration is used to determine the event type returned by <a href="https://msdn.microsoft.com/94ed3028-0bd1-449b-9902-7dbae4a70ec1">DrtGetEventData</a>, which is called with the event handle passed to <a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>.




## -see-also




<a href="https://msdn.microsoft.com/94ed3028-0bd1-449b-9902-7dbae4a70ec1">DrtGetEventData</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 

