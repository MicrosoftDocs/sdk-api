---
UID: NS:audioengineextensionapo.AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
tech.root: audio
title: AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
ms.date: 06/05/2023
targetos: Windows
description: Represents an audio environment change APO notification.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
f1_keywords:
 - AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
 - audioengineextensionapo/AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
dev_langs:
 - c++
helpviewer_keywords:
 - AUDIO_ENVIRONMENT_STATE_CHANGE_NOTIFICATION
---

## -description

Represents an audio environment change APO notification.

## -struct-fields

### -field propertyStore

An [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object representing the property store that the change occurred on. Use this object to query the new value of the property specified in *propertyKey*.

### -field propertyKey

The [PROPERTYKEY](/windows/win32/api/wtypes/ns-wtypes-propertykey) that has a new value.

## -remarks

## -see-also

