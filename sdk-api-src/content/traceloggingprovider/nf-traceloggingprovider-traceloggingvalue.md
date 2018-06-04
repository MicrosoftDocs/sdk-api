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

# TraceLoggingValue macro


## -description


Wrapper macro for event fields. Automatically deduces value type.


## -parameters




### -param value [in]

The event field value.


#### - description [in, optional]

The description of the event field's value. If provided, the description parameter must be a string literal, and will be included in the PDB. 


#### - name [in, optional]

The name of the event field. If provided, the name parameter must be a string literal (not a variable) and must not  contain any '\0' characters.


#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's metadata. The semantics of the tags  are defined by the event consumer. During event processing, this tag can be retrieved from the EVENT_PROPERTY_INFO Tags field. 

