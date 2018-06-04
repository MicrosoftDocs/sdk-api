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

# _DMO_INPUT_DATA_BUFFER_FLAGS enumeration


## -description



The <code>DMO_INPUT_DATA_BUFFER_FLAGS</code> enumeration defines flags that describe an input buffer.




## -enum-fields




### -field DMO_INPUT_DATA_BUFFERF_SYNCPOINT

The beginning of the data is a synchronization point.


### -field DMO_INPUT_DATA_BUFFERF_TIME

The buffer's time stamp is valid.

The buffer's indicated time length is valid.


### -field DMO_INPUT_DATA_BUFFERF_TIMELENGTH

The buffer's indicated time length is valid.


### -field DMO_INPUT_DATA_BUFFERF_DISCONTINUITY




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a>
 

 

