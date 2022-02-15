---
UID: NS:mfapi.tagDigitalWindowSetting
tech.root: mf
title: DigitalWindowSetting
ms.date: 01/11/2021
ms.topic: language-reference
targetos: Windows
description: Represents the bounds settings of the digital window for video capture. 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: DigitalWindowSetting
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - tagDigitalWindowSetting
 - DigitalWindowSetting
f1_keywords:
 - tagDigitalWindowSetting
 - mfapi/tagDigitalWindowSetting
 - DigitalWindowSetting
 - mfapi/DigitalWindowSetting
dev_langs:
 - c++
---

## -description

Represents the bounds settings of the digital window for video capture. 

## -struct-fields

### -field OriginX

The x-axis value of the left side of the digital window bounds.

### -field OriginY

The y-axis value of the top side of the digital window bounds.

### -field WindowSize

A value specifying the scale of the digital window bounds.

## -remarks

This struct is used with the [MF_CAPTURE_METADATA_DIGITALWINDOW](/windows/win32/medfound/mf-capture-metadata-digitalwindow) attribute.

## -see-also

