---
UID: NS:audioenginebaseapo.APOInitSystemEffects2
title: APOInitSystemEffects2 (audioenginebaseapo.h)
description: The APOInitSystemEffects2 structure was introduced with Windows 8.1, to make it possible to provide additional initialization context to the audio processing object (APO) for initialization.
helpviewer_keywords: ["APOInitSystemEffects2","APOInitSystemEffects2 structure [Audio Devices]","PAPOInitSystemEffects2","PAPOInitSystemEffects2 structure pointer [Audio Devices]","audio.apoinitsystemeffects2","audioenginebaseapo/APOInitSystemEffects2","audioenginebaseapo/PAPOInitSystemEffects2"]
old-location: audio\apoinitsystemeffects2.htm
tech.root: audio
ms.assetid: 87E59FCE-1965-4B23-B1F5-F54FEDD5A83E
ms.date: 12/05/2018
ms.keywords: APOInitSystemEffects2, APOInitSystemEffects2 structure [Audio Devices], PAPOInitSystemEffects2, PAPOInitSystemEffects2 structure pointer [Audio Devices], audio.apoinitsystemeffects2, audioenginebaseapo/APOInitSystemEffects2, audioenginebaseapo/PAPOInitSystemEffects2
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
targetos: Windows
req.typenames: APOInitSystemEffects2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APOInitSystemEffects2
 - audioenginebaseapo/APOInitSystemEffects2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioenginebaseapo.h
api_name:
 - APOInitSystemEffects2
---

# APOInitSystemEffects2 structure


## -description

The APOInitSystemEffects2 structure was introduced with Windows 8.1, to make it possible to provide additional initialization context to the audio processing object (APO) for  
initialization.

## -struct-fields

### -field APOInit

An <a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitbasestruct">APOInitBaseStruct</a> structure.

### -field pAPOEndpointProperties

A pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.

### -field pAPOSystemEffectsProperties

A pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> object.

### -field pReserved

Reserved for future use.

### -field pDeviceCollection

A pointer to an IMMDeviceCollection object. The last item in the *pDeviceCollection* is always the [IMMDevice](../mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint.

### -field nSoftwareIoDeviceInCollection

Specifies the MMDevice that implements the DeviceTopology that includes the software connector for which the APO is initializing. The MMDevice is contained in <i>pDeviceCollection</i>.

### -field nSoftwareIoConnectorIndex

Specifies the index of a Software_IO connector in the DeviceTopology.

### -field AudioProcessingMode

Specifies the processing mode for the audio graph.

### -field InitializeForDiscoveryOnly

Indicates whether the audio system is initializing the APO for effects discovery only.

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects">APOInitSystemEffects</a>