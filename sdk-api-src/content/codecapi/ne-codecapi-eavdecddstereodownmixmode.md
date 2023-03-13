---
UID: NE:codecapi.eAVDecDDStereoDownMixMode
title: eAVDecDDStereoDownMixMode (codecapi.h)
description: Specifies the stereo downmix mode for a Dolby Digital audio decoder.
helpviewer_keywords: ["codecapi/eAVDecDDStereoDownMixMode","codecapi/eAVDecDDStereoDownMixMode_Auto","codecapi/eAVDecDDStereoDownMixMode_LoRo","codecapi/eAVDecDDStereoDownMixMode_LtRt","eAVDecDDStereoDownMixMode","eAVDecDDStereoDownMixMode enumeration [Media Foundation]","eAVDecDDStereoDownMixMode_Auto","eAVDecDDStereoDownMixMode_LoRo","eAVDecDDStereoDownMixMode_LtRt","mf.eavdecddstereodownmixmode"]
old-location: mf\eavdecddstereodownmixmode.htm
tech.root: mf
ms.assetid: B7DBC665-2942-433B-8C7F-1A02DB994A8B
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDecDDStereoDownMixMode, codecapi/eAVDecDDStereoDownMixMode_Auto, codecapi/eAVDecDDStereoDownMixMode_LoRo, codecapi/eAVDecDDStereoDownMixMode_LtRt, eAVDecDDStereoDownMixMode, eAVDecDDStereoDownMixMode enumeration [Media Foundation], eAVDecDDStereoDownMixMode_Auto, eAVDecDDStereoDownMixMode_LoRo, eAVDecDDStereoDownMixMode_LtRt, mf.eavdecddstereodownmixmode
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - eAVDecDDStereoDownMixMode
 - codecapi/eAVDecDDStereoDownMixMode
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
 - eAVDecDDStereoDownMixMode
---

# eAVDecDDStereoDownMixMode enumeration


## -description

Specifies the stereo downmix mode for a Dolby Digital audio decoder. This enumeration is used with the <a href="/windows/desktop/medfound/codecapi-avdecddstereodownmixmode">CODECAPI_AVDecDDStereoDownMixMode</a> property.

## -enum-fields

### -field eAVDecDDStereoDownMixMode_Auto:0

The decoder selects the mode automatically.

### -field eAVDecDDStereoDownMixMode_LtRt:1

Left total/right total (Lt/Rt) downmix. (Surround compatible.)

### -field eAVDecDDStereoDownMixMode_LoRo:2  

Left only/right only (Lo/Ro) downmix. (Stereo.)

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
