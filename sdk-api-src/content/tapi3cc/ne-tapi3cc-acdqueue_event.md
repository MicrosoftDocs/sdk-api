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

# ACDQUEUE_EVENT enumeration


## -description


The 
<b>ACDQUEUE_EVENT</b> enum describes ACD queue events. The 
<a href="https://msdn.microsoft.com/704a9601-e8c3-42d4-86bc-be59c44a05b3">ITQueueEvent::get_Event</a> method returns a member of this enum to indicate the type of ACD queue event that occurred.


## -enum-fields




### -field ACDQE_NEW_QUEUE

A new ACD queue has been added.


### -field ACDQE_QUEUE_REMOVED

An ACD queue has been removed.


## -see-also




<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>



<a href="https://msdn.microsoft.com/08a3925c-e14e-442e-952e-483fc41d049c">ITCallNotificationEvent::get_Event</a>



<a href="https://msdn.microsoft.com/704a9601-e8c3-42d4-86bc-be59c44a05b3">ITQueueEvent::get_Event</a>
 

 

