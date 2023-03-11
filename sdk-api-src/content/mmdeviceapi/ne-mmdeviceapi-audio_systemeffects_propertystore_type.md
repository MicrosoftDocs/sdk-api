---
UID: NE:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0008_0002
tech.root: audio
title: AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE
ms.date: 06/18/2021
targetos: Windows
description: Specifies the type of an audio system effects property store.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mmdeviceapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mmdeviceapi.h
api_name:
 - __MIDL___MIDL_itf_mmdeviceapi_0000_0008_0002
 - AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE
f1_keywords:
 - __MIDL___MIDL_itf_mmdeviceapi_0000_0008_0002
 - mmdeviceapi/__MIDL___MIDL_itf_mmdeviceapi_0000_0008_0002
 - AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE
 - mmdeviceapi/AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE
dev_langs:
 - c++
---

## -description

Specifies the type of an audio system effects property store.

## -enum-fields

### -field AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE_DEFAULT

Default property store. Contains custom effects properties and is populated from the INF file. Properties will not be persisted across OS upgrades.

### -field AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE_USER

User property store. Contains user settings pertaining to effects properties and will be persisted by the OS across upgrades and migrations.

### -field AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE_VOLATILE

The volatile property store. Contains audio effects properties that are lost on device reboot. The store is cleared each time the endpoint transitions to active

### -field AUDIO_SYSTEMEFFECTS_PROPERTYSTORE_TYPE_ENUM_COUNT

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

