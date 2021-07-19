---
UID: NS:audioengineextensionapo.APOInitSystemEffects3
tech.root: audio
title: APOInitSystemEffects3
ms.date: 06/19/2021
targetos: Windows
description: Provide additional initialization context to the audio processing object (APO) for  
initialization, adding support for specifying a logging service provider.
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: APOInitSystemEffects3
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - APOInitSystemEffects3
f1_keywords:
 - APOInitSystemEffects3
 - audioengineextensionapo/APOInitSystemEffects3
dev_langs:
 - c++
---

## -description

Provide additional initialization context to the audio processing object (APO) for  
initialization, adding support for specifying a logging service provider.

## -struct-fields

### -field APOInit

An [APOInitBaseStruct](../audioenginebaseapo/ns-audioenginebaseapo-apoinitbasestruct.md) structure.

### -field pAPOEndpointProperties

A pointer to an [IPropertyStore](/propsys/nn-propsys-ipropertystore.md) object.

### -field pServiceProvider

An [IServiceProvider](../servprov/nn-servprov-iserviceprovider.md) representing a service provider such as [IAudioProcessingObjectLoggingService] or [IAudioProcessingObjectRTQueueService](nn-audioengineextensionapo-iaudioprocessingobjectrtqueueservice.md).

### -field pDeviceCollection

A pointer to an IMMDeviceCollection object. The last item in the *pDeviceCollection* is always the [IMMDevice](../mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint.

### -field nSoftwareIoDeviceInCollection

Specifies the MMDevice that implements the DeviceTopology that includes the software connector for which the APO is initializing. The MMDevice is contained in *pDeviceCollection*.

### -field nSoftwareIoConnectorIndex

Specifies the index of a Software_IO connector in the DeviceTopology.

### -field AudioProcessingMode

Specifies the processing mode for the audio graph.

### -field InitializeForDiscoveryOnly

Indicates whether the audio system is initializing the APO for effects discovery only.

## -remarks

If a client implements [IAudioSystemEffects3](nn-audioengineextensionapo-iaudiosystemeffects3.md), an **APOInitSystemEffects3** structure is passed into the [IAudioProcessingObject::Initialize](..//audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize.md) method.

> [!NOTE] On OS versions earlier than Windows Build 22000, the system will not pass an **APOInitSystemEffects3** into **IAudioProcessingObject::Initialize** even if the client implements **IAudioSystemEffects3**, but will instead pass an older version of the structure, [APOInitSystemEffects2](audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2) or [APOInitSystemEffects](audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2), into **Initialize**.

## -see-also

[APOInitSystemEffects](../audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects.md)

[APOInitSystemEffects2](../audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2.md)

