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

# _CERT_TRUST_LIST_INFO structure


## -description


The <b>CERT_TRUST_LIST_INFO</b> structure that indicates valid usage of a CTL.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field pCtlEntry

A pointer to a structure that includes a subject identifier, the count of attributes associated with a CTL, and an array of those attributes.


### -field pCtlContext

A pointer to a CTL context.


## -see-also




<a href="https://msdn.microsoft.com/a1f6ba18-63ef-43ac-a17f-900fa13398aa">CERT_CHAIN_ELEMENT</a>



<a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a>
 

 

