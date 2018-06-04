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

# _MIB_OPAQUE_INFO structure


## -description


The 
<b>MIB_OPAQUE_INFO</b> structure contains information returned from a MIB opaque query.


## -struct-fields




### -field dwId

The type of information returned.


### -field ullAlign

The number of bytes that align the information returned.


### -field rgbyData

A pointer to the information returned from the opaque query.


## -see-also




<a href="https://msdn.microsoft.com/cd87cbe4-3da4-4205-9a88-becf4f341ab5">MIB_OPAQUE_QUERY</a>
 

 

