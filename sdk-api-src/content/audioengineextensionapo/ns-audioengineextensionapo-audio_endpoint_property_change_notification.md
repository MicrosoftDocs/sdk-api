---
UID: NS:audioengineextensionapo.AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION
tech.root: audio
title: AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION
ms.date: 06/18/2021
targetos: Windows
description: Represents a property change APO notification.
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
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION
f1_keywords:
 - AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION
 - audioengineextensionapo/AUDIO_ENDPOINT_PROPERTY_CHANGE_NOTIFICATION
dev_langs:
 - c++
---

## -description

Represents a property change APO notification.

## -struct-fields

### -field endpoint

An [IMMDevice](../mmdeviceapi/nn-mmdeviceapi-immdevice.md) representing the audio endpoint associated with the notification.

### -field propertyStore

An [IPropertyStore](../propsys/nn-propsys-ipropertystore.md) representing the property store associated with the notification.

### -field propertyKey

A [PROPERTYKEY](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure identifying the property associated with the notification.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

