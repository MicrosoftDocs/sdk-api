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

# _DMO_SET_TYPE_FLAGS enumeration


## -description



The <code>DMO_SET_TYPE_FLAGS</code> enumeration defines flags for setting the media type on a stream.




## -enum-fields




### -field DMO_SET_TYPEF_TEST_ONLY

Test the media type but do not set it.


### -field DMO_SET_TYPEF_CLEAR

Clear the media type that was set for the stream.


## -remarks



The DMO_SET_TYPEF_TEST_ONLY and DMO_SET_TYPEF_CLEAR flags are mutually exclusive. Do not set both flags.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/6b466fe4-97a0-46f9-9e4b-461ee66095f1">IMediaObject::SetInputType</a>



<a href="https://msdn.microsoft.com/1dda3c55-d37b-4e04-9509-0e5197d6b019">IMediaObject::SetOutputType</a>
 

 

