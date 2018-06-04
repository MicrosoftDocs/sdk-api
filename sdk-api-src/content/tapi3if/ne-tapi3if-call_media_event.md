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

# CALL_MEDIA_EVENT enumeration


## -description


The 
<b>CALL_MEDIA_EVENT</b> enum describes call media events. The 
<a href="https://msdn.microsoft.com/3dd6210f-e904-46c5-8fc3-50a62b8754ed">ITCallMediaEvent::get_Event</a> method returns a member of this enum to indicate the type of call media event that occurred.


## -enum-fields




### -field CME_NEW_STREAM

A new media stream has been created.


### -field CME_STREAM_FAIL

A media stream or stream request has failed.


### -field CME_TERMINAL_FAIL

A terminal has failed.


### -field CME_STREAM_NOT_USED

The media stream has not been used.


### -field CME_STREAM_ACTIVE

The media stream is active.


### -field CME_STREAM_INACTIVE

The media stream is not active.


### -field CME_LASTITEM




## -remarks



Due to latency, stream events may continue for a few seconds after a stream or related call session has been torn down.




## -see-also




<a href="https://msdn.microsoft.com/3dd6210f-e904-46c5-8fc3-50a62b8754ed">ITCallMediaEvent::get_Event</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

