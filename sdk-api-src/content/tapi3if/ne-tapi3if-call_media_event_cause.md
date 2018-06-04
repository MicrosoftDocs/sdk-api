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

# CALL_MEDIA_EVENT_CAUSE enumeration


## -description


The 
<b>CALL_MEDIA_EVENT_CAUSE</b> enum is used by 
<a href="https://msdn.microsoft.com/51905e69-ff95-46fb-a73a-785a8d444253">ITCallMediaEvent::get_Cause</a> method to return a description of what caused a media event, such as a device timeout.


## -enum-fields




### -field CMC_UNKNOWN

Call media is unknown.


### -field CMC_BAD_DEVICE

Device source or renderer is not functioning.


### -field CMC_CONNECT_FAIL

Could not connect to media device.


### -field CMC_LOCAL_REQUEST

A local request has been received.


### -field CMC_REMOTE_REQUEST

A remote request has been received.


### -field CMC_MEDIA_TIMEOUT

The media device timed out.


### -field CMC_MEDIA_RECOVERED

Media processing has resumed after an interruption.


### -field CMC_QUALITY_OF_SERVICE




## -see-also




<a href="https://msdn.microsoft.com/51905e69-ff95-46fb-a73a-785a8d444253">ITCallMediaEvent::get_Cause</a>
 

 

