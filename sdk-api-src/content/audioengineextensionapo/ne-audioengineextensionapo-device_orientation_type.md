---
UID: NE:audioengineextensionapo.DEVICE_ORIENTATION_TYPE
tech.root: audio
title: DEVICE_ORIENTATION_TYPE
ms.date: 02/28/2023
targetos: Windows
description: Specifies device orientation values for notifications of type APO_NOTIFICATION_TYPE_DEVICE_ORIENTATION.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: audioengineextensionapo.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows build 22621
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioengineextensionapo.h
api_name:
 - DEVICE_ORIENTATION_TYPE
f1_keywords:
 - DEVICE_ORIENTATION_TYPE
 - audioengineextensionapo/DEVICE_ORIENTATION_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - DEVICE_ORIENTATION_TYPE
---

## -description

Specifies device orientation values for notifications of type [APO_NOTIFICATION_TYPE_DEVICE_ORIENTATION](./ne-audioengineextensionapo-apo_notification_type.md).

## -enum-fields

### -field DEVICE_NOT_ROTATED

The device is not rotated

### -field DEVICE_ROTATED_90_DEGREES_CLOCKWISE

The device is rotated 90 degrees clockwise.

### -field DEVICE_ROTATED_180_DEGREES_CLOCKWISE

The device is rotated 180 degrees clockwise.

### -field DEVICE_ROTATED_270_DEGREES_CLOCKWISE

The device is rotated 180 degrees clockwise.

## -remarks

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

