---
UID: NE:tapi3.ACDQUEUE_EVENT
title: ACDQUEUE_EVENT (tapi3.h)
author: windows-sdk-content
description: The ACDQUEUE_EVENT enum describes ACD queue events. The ITQueueEvent::get_Event method returns a member of this enum to indicate the type of ACD queue event that occurred.
old-location: tapi3\acdqueue_event.htm
tech.root: Tapi
ms.assetid: 5a2efb70-a943-46c5-a362-18579ad8c965
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ACDQE_NEW_QUEUE, ACDQE_QUEUE_REMOVED, ACDQUEUE_EVENT, ACDQUEUE_EVENT enumeration [TAPI 2.2], _tapi3_acdqueue_event, tapi3.acdqueue_event, tapi3cc/ACDQE_NEW_QUEUE, tapi3cc/ACDQE_QUEUE_REMOVED, tapi3cc/ACDQUEUE_EVENT
ms.topic: enum
f1_keywords: 
 - "tapi3/ACDQUEUE_EVENT"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: ACDQUEUE_EVENT
req.redist: 
ms.custom: 19H1
---

# ACDQUEUE_EVENT enumeration


## -description


The 
<b>ACDQUEUE_EVENT</b> enum describes ACD queue events. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueueevent-get_event">ITQueueEvent::get_Event</a> method returns a member of this enum to indicate the type of ACD queue event that occurred.


## -enum-fields




### -field ACDQE_NEW_QUEUE

A new ACD queue has been added.


### -field ACDQE_QUEUE_REMOVED

An ACD queue has been removed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallnotificationevent-get_event">ITCallNotificationEvent::get_Event</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itqueueevent-get_event">ITQueueEvent::get_Event</a>
 

 

