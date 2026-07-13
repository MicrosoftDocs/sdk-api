---
UID: NF:mmdeviceapi.IAudioSystemEffectsPropertyChangeNotificationClient.OnPropertyChanged
tech.root: audio
title: IAudioSystemEffectsPropertyChangeNotificationClient::OnPropertyChanged
ms.date: 06/18/2021
targetos: Windows
description: Called by the system when an audio system effects property changes.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mmdeviceapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mmdeviceapi.h
api_name:
 - IAudioSystemEffectsPropertyChangeNotificationClient::OnPropertyChanged
f1_keywords:
 - IAudioSystemEffectsPropertyChangeNotificationClient::OnPropertyChanged
 - mmdeviceapi/IAudioSystemEffectsPropertyChangeNotificationClient::OnPropertyChanged
dev_langs:
 - c++
---

## -description

Called by the system when an audio system effects property changes.

## -parameters

### -param type

A value from the [AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE](ne-mmdeviceapi-audio_systemeffects_propertystore_type.md) specifying the type of the property store that triggered the callback.
 
### -param key

A [PROPERTYKEY](../wtypes/ns-wtypes-propertykey.md) structure identifying the property that changed.

## -returns

## -remarks

Register to receive callbacks by calling [IAudioSystemEffectsPropertyStore::RegisterPropertyChangeNotification](nf-mmdeviceapi-iaudiosystemeffectspropertystore-registerpropertychangenotification.md). Unregister the callback interface by calling [IAudioSystemEffectsPropertyStore::UnregisterPropertyChangeNotification](nf-mmdeviceapi-iaudiosystemeffectspropertystore-unregisterpropertychangenotification.md).

This method will not be called if the registry is manually edited. A notification is generated only when [IPropertyStore::SetValue](../propsys/nf-propsys-ipropertystore-setvalue.md) is called on the associated default, user, or volatile property store.

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

