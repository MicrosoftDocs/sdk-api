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

# _MFRR_COMPONENTS structure


## -description



Contains information about one or more revoked components.




## -struct-fields




### -field dwRRInfoVersion

Revocation information version.


### -field dwRRComponents

Number of elements in the <b>pRRComponents</b> array.


### -field pRRComponents

Array of <a href="https://msdn.microsoft.com/e23bc68c-b62e-4483-b2a7-a7de7376697f">MFRR_COMPONENT_HASH_INFO</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/e23bc68c-b62e-4483-b2a7-a7de7376697f">MFRR_COMPONENT_HASH_INFO</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

