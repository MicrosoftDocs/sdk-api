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

# TraceLoggingCustomAttribute macro


## -description


Wrapper macro for adding custom information about an event to the PDB.


## -parameters




### -param key [in]

The key for the custom attribute.


### -param value [in]

The value of the custom attribute.


## -remarks



Both parameters must be string literals. This information  will appear under the CustomAttributes array for the event. If no custom  attributes are specified the array will not appear. Multiple custom attributes  can be specified per event.  

Custom attributes are stored in the PDB. They are not available at runtime.



