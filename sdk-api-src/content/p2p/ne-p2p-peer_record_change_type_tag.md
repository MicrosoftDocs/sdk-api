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

# peer_record_change_type_tag enumeration


## -description


The <b>PEER_RECORD_CHANGE_TYPE</b> enumeration specifies the changes that can occur to a record.


## -enum-fields




### -field PEER_RECORD_ADDED

Indicates that the specified record is added to the peer graph or group.


### -field PEER_RECORD_UPDATED

Indicates that the specified record is updated in the peer graph or group.


### -field PEER_RECORD_DELETED

Indicates that the specified record is deleted from the peer graph or group.


### -field PEER_RECORD_EXPIRED

Indicates that the specified record is expired and removed from the peer graph or group.


## -see-also




<a href="https://msdn.microsoft.com/01404fff-3488-43aa-bc59-3e08ff925ea5">
        PEER_EVENT_RECORD_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/454b40f6-a7de-4b59-ae35-a809c4510133">
        PFNPEER_SECURE_RECORD</a>



<a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">
        PFNPEER_VALIDATE_RECORD</a>
 

 

