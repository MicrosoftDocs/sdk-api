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

# _MF_TOPONODE_DRAIN_MODE enumeration


## -description



Defines at what times a transform in a topology is drained.




## -enum-fields




### -field MF_TOPONODE_DRAIN_DEFAULT

The transform is drained when the end of a stream is reached. It is not drained when markout is reached at the end of a segment.


### -field MF_TOPONODE_DRAIN_ALWAYS

The transform is drained whenever a topology ends.


### -field MF_TOPONODE_DRAIN_NEVER

The transform is never drained.


## -see-also




<a href="https://msdn.microsoft.com/68332106-d1fe-467b-8baa-1e592b9cc243">MF_TOPONODE_DRAIN</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

