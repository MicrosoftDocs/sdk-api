---
UID: NS:audioenginebaseapo.APOInitSystemEffects2
title: APOInitSystemEffects2
author: windows-sdk-content
description: The APOInitSystemEffects2 structure was introduced with Windows 8.1, to make it possible to provide additional initialization context to the audio processing object (APO) for initialization.
old-location: audio\apoinitsystemeffects2.htm
tech.root: audio
ms.assetid: 87E59FCE-1965-4B23-B1F5-F54FEDD5A83E
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: APOInitSystemEffects2, APOInitSystemEffects2 structure [Audio Devices], PAPOInitSystemEffects2, PAPOInitSystemEffects2 structure pointer [Audio Devices], audio.apoinitsystemeffects2, audioenginebaseapo/APOInitSystemEffects2, audioenginebaseapo/PAPOInitSystemEffects2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioenginebaseapo.h
api_name:
 - APOInitSystemEffects2
product: Windows
targetos: Windows
req.typenames: APOInitSystemEffects2
req.redist: 
---

# APOInitSystemEffects2 structure


## -description


The APOInitSystemEffects2 structure was introduced with Windows 8.1, to make it possible to provide additional initialization context to the audio processing object (APO) for  
initialization.


## -struct-fields




### -field APOInit

An <a href="https://msdn.microsoft.com/15C973AE-B0E8-42FD-9F34-671A6A915B47">APOInitBaseStruct</a> structure.


### -field pAPOEndpointProperties

A pointer to an <a href="https://msdn.microsoft.com/63afd5b1-87cc-4e0a-8964-2138c5fbff46">IPropertyStore</a> object.


### -field pAPOSystemEffectsProperties

A pointer to an <a href="https://msdn.microsoft.com/63afd5b1-87cc-4e0a-8964-2138c5fbff46">IPropertyStore</a> object.


### -field pReserved

Reserved for future use.


### -field pDeviceCollection

A pointer to an IMMDeviceCollection object.


### -field nSoftwareIoDeviceInCollection

Specifies the MMDevice that implements the DeviceTopology that includes the software connector for which the APO is initializing. The MMDevice is contained in <i>pDeviceCollection</i>.


### -field nSoftwareIoConnectorIndex

Specifies the index of a Software_IO connector in the DeviceTopology.


### -field AudioProcessingMode

Specifies the processing mode for the audio graph.


### -field InitializeForDiscoveryOnly

Indicates whether the audio system is initializing the APO for effects discovery only.


## -see-also




<a href="https://msdn.microsoft.com/E33B1F94-4E3A-4EC1-AFB5-FD803FA391BC">APOInitSystemEffects</a>
 

 

