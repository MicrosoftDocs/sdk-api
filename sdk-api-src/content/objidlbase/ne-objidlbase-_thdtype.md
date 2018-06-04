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

# _THDTYPE enumeration


## -description


Indicates whether a particular thread supports a message loop.


## -enum-fields




### -field THDTYPE_BLOCKMESSAGES

The thread does not support a message loop. This behavior is associated with multithreaded apartments.


### -field THDTYPE_PROCESSMESSAGES

The thread supports a message loop. This behavior is associated with single-threaded apartments.


## -see-also




<a href="https://msdn.microsoft.com/93437e45-f1e7-4f1f-bffb-ef234c7f5a6b">IComThreadingInfo::GetCurrentThreadType</a>
 

 

