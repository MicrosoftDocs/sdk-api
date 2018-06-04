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

# APOInitSystemEffects structure


## -description


The APOInitSystemEffects structure gets passed to the system effects APO for  
initialization.


## -struct-fields




### -field APOInit

An <a href="https://msdn.microsoft.com/library/windows/hardware/jj151545">APOInitBaseStruct</a> structure.


### -field pAPOEndpointProperties

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


### -field pAPOSystemEffectsProperties

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


### -field pReserved

Reserved for future use.


### -field pDeviceCollection

A pointer to an IMMDeviceCollection object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj151545">APOInitBaseStruct</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn659347">APOInitSystemEffects2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>
 

 

