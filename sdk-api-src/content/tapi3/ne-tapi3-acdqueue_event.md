---
UID: NE:tapi3.ACDQUEUE_EVENT
title: ACDQUEUE_EVENT
author: windows-sdk-content
description: The ACDQUEUE_EVENT enum describes ACD queue events. The ITQueueEvent::get_Event method returns a member of this enum to indicate the type of ACD queue event that occurred.
old-location: tapi3\acdqueue_event.htm
tech.root: tapi
ms.assetid: 5a2efb70-a943-46c5-a362-18579ad8c965
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ACDQE_NEW_QUEUE, ACDQE_QUEUE_REMOVED, ACDQUEUE_EVENT, ACDQUEUE_EVENT enumeration [TAPI 2.2], _tapi3_acdqueue_event, tapi3.acdqueue_event, tapi3cc/ACDQE_NEW_QUEUE, tapi3cc/ACDQE_QUEUE_REMOVED, tapi3cc/ACDQUEUE_EVENT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tapi3cc.h
api_name:
 - ACDQUEUE_EVENT
product: Windows
targetos: Windows
req.typenames: ACDQUEUE_EVENT
req.redist: 
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
 

 

