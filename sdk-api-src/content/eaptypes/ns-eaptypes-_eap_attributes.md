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

# _EAP_ATTRIBUTES structure


## -description


The <b>EAP_ATTRIBUTES</b> structure contains an array of EAP attributes.


## -struct-fields




### -field dwNumberOfAttributes

The number of <a href="https://msdn.microsoft.com/a8fe754a-ce6f-45f4-9536-7ffda2183e9e">EAP_ATTRIBUTE</a> structures in <b>pAttribs</b>.


### -field pAttribs.size_is

 


### -field pAttribs.size_is.dwNumberOfAttributes

 


### -field pAttribs

Pointer to the address of the first element in an array of <a href="https://msdn.microsoft.com/a8fe754a-ce6f-45f4-9536-7ffda2183e9e">EAP_ATTRIBUTE</a> structures. The total number of elements is specified in <b>dwNumberOfAttributes</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/a8fe754a-ce6f-45f4-9536-7ffda2183e9e">EAP_ATTRIBUTE</a>
 

 

