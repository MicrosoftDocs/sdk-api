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

# tagKSP_PINMODE structure


## -description


The KSP_PINMODE structure specifies the pin property and the supported audio processing modes for a pin factory.

KSP_PINMODE provides property data for <a href="https://msdn.microsoft.com/library/windows/hardware/dn457706">KSPROPERTY_AUDIOEFFECTSDISCOVERY_EFFECTSLIST</a>.


## -struct-fields




### -field PinProperty

The pin property of the pin factory.


### -field AudioProcessingMode

The audio processing mode (or modes) supported by the pin factory.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn457706">KSPROPERTY_AUDIOEFFECTSDISCOVERY_EFFECTSLIST</a>
 

 

