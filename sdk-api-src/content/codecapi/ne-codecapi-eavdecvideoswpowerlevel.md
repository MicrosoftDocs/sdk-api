---
UID: NE:codecapi.eAVDecVideoSWPowerLevel
title: eAVDecVideoSWPowerLevel (codecapi.h)
description: Specifies the power-saving level of a video decoder.
helpviewer_keywords: ["codecapi/eAVDecVideoSWPowerLevel","codecapi/eAVDecVideoSWPowerLevel_Balanced","codecapi/eAVDecVideoSWPowerLevel_BatteryLife","codecapi/eAVDecVideoSWPowerLevel_VideoQuality","dshow.eavdecvideoswpowerlevel","eAVDecVideoSWPowerLevel","eAVDecVideoSWPowerLevel enumeration [DirectShow]","eAVDecVideoSWPowerLevel_Balanced","eAVDecVideoSWPowerLevel_BatteryLife","eAVDecVideoSWPowerLevel_VideoQuality"]
old-location: dshow\eavdecvideoswpowerlevel.htm
tech.root: dshow
ms.assetid: bf1c4c79-8e45-43ac-a203-444a00240eed
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDecVideoSWPowerLevel, codecapi/eAVDecVideoSWPowerLevel_Balanced, codecapi/eAVDecVideoSWPowerLevel_BatteryLife, codecapi/eAVDecVideoSWPowerLevel_VideoQuality, dshow.eavdecvideoswpowerlevel, eAVDecVideoSWPowerLevel, eAVDecVideoSWPowerLevel enumeration [DirectShow], eAVDecVideoSWPowerLevel_Balanced, eAVDecVideoSWPowerLevel_BatteryLife, eAVDecVideoSWPowerLevel_VideoQuality
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
 - eAVDecVideoSWPowerLevel
 - codecapi/eAVDecVideoSWPowerLevel
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
 - eAVDecVideoSWPowerLevel
---

# eAVDecVideoSWPowerLevel enumeration


## -description

Specifies the power-saving level of a video decoder. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property">AVDecVideoSWPowerLevel</a> property.

## -enum-fields

### -field eAVDecVideoSWPowerLevel_BatteryLife:0

Optimize for battery life.

### -field eAVDecVideoSWPowerLevel_Balanced:50

Balanced power-saving profile.

### -field eAVDecVideoSWPowerLevel_VideoQuality:100

Optimize for video quality.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
