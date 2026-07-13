---
UID: NS:audioengineextensionapo.APOInitSystemEffects3
tech.root: audio
title: APOInitSystemEffects3
ms.date: 10/19/2021
targetos: Windows
description: Provides APO initialization parameters, extending APOInitSystemEffects2 to add the ability to specify a service provider for logging.
prerelease: false
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
req.target-min-winversvr: Windows Build 22000
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

Provides audio processing object (APO) initialization parameters, extending [APOInitSystemEffects2](../audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2.md) to add the ability to specify a service provider for logging.

## -struct-fields

### -field APOInit

An [APOInitBaseStruct](../audioenginebaseapo/ns-audioenginebaseapo-apoinitbasestruct.md) structure.

### -field pAPOEndpointProperties

A pointer to an [IPropertyStore](../propsys/nn-propsys-ipropertystore.md) object.

### -field pServiceProvider

An [IServiceProvider](../servprov/nn-servprov-iserviceprovider.md) interface.

### -field pDeviceCollection

A pointer to an [IMMDeviceCollection](../mmdeviceapi/nn-mmdeviceapi-immdevicecollection.md) object. The last item in the *pDeviceCollection* is always the [IMMDevice](../mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint.

### -field nSoftwareIoDeviceInCollection

Specifies the **MMDevice** that implements the DeviceTopology that includes the software connector for which the APO is initializing. The **MMDevice** is contained in *pDeviceCollection*.

### -field nSoftwareIoConnectorIndex

Specifies the index of a **Software_IO** connector in the [DeviceTopology](../devicetopology/nn-devicetopology-idevicetopology.md).

### -field AudioProcessingMode

Specifies the processing mode for the audio graph.

### -field InitializeForDiscoveryOnly

Indicates whether the audio system is initializing the APO for effects discovery only.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).


## -see-also

[APOInitSystemEffects](../audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects.md)
[APOInitSystemEffects2](../audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2.md)

