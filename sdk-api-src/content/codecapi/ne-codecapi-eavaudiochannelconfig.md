---
UID: NE:codecapi.eAVAudioChannelConfig
title: eAVAudioChannelConfig (codecapi.h)
description: Specifies the speaker configuration for the audio channels in the audio bit stream. This enumeration is used with the AVAudioChannelConfig property.
helpviewer_keywords: ["codecapi/eAVAudioChannelConfig","codecapi/eAVAudioChannelConfig_BACK_CENTER","codecapi/eAVAudioChannelConfig_BACK_LEFT","codecapi/eAVAudioChannelConfig_BACK_RIGHT","codecapi/eAVAudioChannelConfig_FRONT_CENTER","codecapi/eAVAudioChannelConfig_FRONT_LEFT","codecapi/eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER","codecapi/eAVAudioChannelConfig_FRONT_RIGHT","codecapi/eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER","codecapi/eAVAudioChannelConfig_LOW_FREQUENCY","codecapi/eAVAudioChannelConfig_SIDE_LEFT","codecapi/eAVAudioChannelConfig_SIDE_RIGHT","codecapi/eAVAudioChannelConfig_TOP_BACK_CENTER","codecapi/eAVAudioChannelConfig_TOP_BACK_LEFT","codecapi/eAVAudioChannelConfig_TOP_BACK_RIGHT","codecapi/eAVAudioChannelConfig_TOP_CENTER","codecapi/eAVAudioChannelConfig_TOP_FRONT_CENTER","codecapi/eAVAudioChannelConfig_TOP_FRONT_LEFT","codecapi/eAVAudioChannelConfig_TOP_FRONT_RIGHT","dshow.eavaudiochannelconfig","eAVAudioChannelConfig","eAVAudioChannelConfig enumeration [DirectShow]","eAVAudioChannelConfigEnumeration","eAVAudioChannelConfig_BACK_CENTER","eAVAudioChannelConfig_BACK_LEFT","eAVAudioChannelConfig_BACK_RIGHT","eAVAudioChannelConfig_FRONT_CENTER","eAVAudioChannelConfig_FRONT_LEFT","eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER","eAVAudioChannelConfig_FRONT_RIGHT","eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER","eAVAudioChannelConfig_LOW_FREQUENCY","eAVAudioChannelConfig_SIDE_LEFT","eAVAudioChannelConfig_SIDE_RIGHT","eAVAudioChannelConfig_TOP_BACK_CENTER","eAVAudioChannelConfig_TOP_BACK_LEFT","eAVAudioChannelConfig_TOP_BACK_RIGHT","eAVAudioChannelConfig_TOP_CENTER","eAVAudioChannelConfig_TOP_FRONT_CENTER","eAVAudioChannelConfig_TOP_FRONT_LEFT","eAVAudioChannelConfig_TOP_FRONT_RIGHT"]
old-location: dshow\eavaudiochannelconfig.htm
tech.root: dshow
ms.assetid: 8835b00b-048b-404a-9ecc-84baeb70df66
ms.date: 12/05/2018
ms.keywords: codecapi/eAVAudioChannelConfig, codecapi/eAVAudioChannelConfig_BACK_CENTER, codecapi/eAVAudioChannelConfig_BACK_LEFT, codecapi/eAVAudioChannelConfig_BACK_RIGHT, codecapi/eAVAudioChannelConfig_FRONT_CENTER, codecapi/eAVAudioChannelConfig_FRONT_LEFT, codecapi/eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER, codecapi/eAVAudioChannelConfig_FRONT_RIGHT, codecapi/eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER, codecapi/eAVAudioChannelConfig_LOW_FREQUENCY, codecapi/eAVAudioChannelConfig_SIDE_LEFT, codecapi/eAVAudioChannelConfig_SIDE_RIGHT, codecapi/eAVAudioChannelConfig_TOP_BACK_CENTER, codecapi/eAVAudioChannelConfig_TOP_BACK_LEFT, codecapi/eAVAudioChannelConfig_TOP_BACK_RIGHT, codecapi/eAVAudioChannelConfig_TOP_CENTER, codecapi/eAVAudioChannelConfig_TOP_FRONT_CENTER, codecapi/eAVAudioChannelConfig_TOP_FRONT_LEFT, codecapi/eAVAudioChannelConfig_TOP_FRONT_RIGHT, dshow.eavaudiochannelconfig, eAVAudioChannelConfig, eAVAudioChannelConfig enumeration [DirectShow], eAVAudioChannelConfigEnumeration, eAVAudioChannelConfig_BACK_CENTER, eAVAudioChannelConfig_BACK_LEFT, eAVAudioChannelConfig_BACK_RIGHT, eAVAudioChannelConfig_FRONT_CENTER, eAVAudioChannelConfig_FRONT_LEFT, eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER, eAVAudioChannelConfig_FRONT_RIGHT, eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER, eAVAudioChannelConfig_LOW_FREQUENCY, eAVAudioChannelConfig_SIDE_LEFT, eAVAudioChannelConfig_SIDE_RIGHT, eAVAudioChannelConfig_TOP_BACK_CENTER, eAVAudioChannelConfig_TOP_BACK_LEFT, eAVAudioChannelConfig_TOP_BACK_RIGHT, eAVAudioChannelConfig_TOP_CENTER, eAVAudioChannelConfig_TOP_FRONT_CENTER, eAVAudioChannelConfig_TOP_FRONT_LEFT, eAVAudioChannelConfig_TOP_FRONT_RIGHT
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVAudioChannelConfig
 - codecapi/eAVAudioChannelConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVAudioChannelConfig
---

# eAVAudioChannelConfig enumeration


## -description

Specifies the speaker configuration for the audio channels in the audio bit stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avaudiochannelconfig-property">AVAudioChannelConfig</a> property.

## -enum-fields

### -field eAVAudioChannelConfig_FRONT_LEFT:0x1

Front left

### -field eAVAudioChannelConfig_FRONT_RIGHT:0x2

Front right

### -field eAVAudioChannelConfig_FRONT_CENTER:0x4

Front center

### -field eAVAudioChannelConfig_LOW_FREQUENCY:0x8

Low frequency effect (LFE)

### -field eAVAudioChannelConfig_BACK_LEFT:0x10

Back left

### -field eAVAudioChannelConfig_BACK_RIGHT:0x20

Back right

### -field eAVAudioChannelConfig_FRONT_LEFT_OF_CENTER:0x40

Front, left of center

### -field eAVAudioChannelConfig_FRONT_RIGHT_OF_CENTER:0x80

Front, right of center

### -field eAVAudioChannelConfig_BACK_CENTER:0x100

Back center

### -field eAVAudioChannelConfig_SIDE_LEFT:0x200

Side left

### -field eAVAudioChannelConfig_SIDE_RIGHT:0x400

Side right

### -field eAVAudioChannelConfig_TOP_CENTER:0x800

Top center

### -field eAVAudioChannelConfig_TOP_FRONT_LEFT:0x1000

Top, front left

### -field eAVAudioChannelConfig_TOP_FRONT_CENTER:0x2000

Top, front center

### -field eAVAudioChannelConfig_TOP_FRONT_RIGHT:0x4000

Top, front right

### -field eAVAudioChannelConfig_TOP_BACK_LEFT:0x8000

Top, back left

### -field eAVAudioChannelConfig_TOP_BACK_CENTER:0x10000

Top, back center

### -field eAVAudioChannelConfig_TOP_BACK_RIGHT:0x20000 

Top, back right

## -remarks

These values correspond to the flags used for the <b>dwChannelMask</b> member of the <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)">WAVEFORMATEXTENSIBLE</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
