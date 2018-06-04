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

# _IMAPI_FORMAT2_TAO_WRITE_ACTION enumeration


## -description


Defines values that indicate the current state of the write operation when using the <a href="https://msdn.microsoft.com/4bbcc3e1-0c85-4ed8-bbf6-e172e5896ed9">IDiscFormat2TrackAtOnceEventArgs</a> interface.


## -enum-fields




### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_UNKNOWN

Indicates an unknown state.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_PREPARING

Preparing to write the track.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_WRITING

Writing the track.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_FINISHING

Closing the track or closing the session.


### -field IMAPI_FORMAT2_TAO_WRITE_ACTION_VERIFYING




## -see-also




<a href="https://msdn.microsoft.com/d63ff41d-993c-4f42-a4a3-f7c67f292a03">DDiscFormat2TrackAtOnceEvents::Update</a>
 

 

