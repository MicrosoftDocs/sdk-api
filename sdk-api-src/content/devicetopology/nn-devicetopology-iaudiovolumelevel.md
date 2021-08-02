---
UID: NN:devicetopology.IAudioVolumeLevel
title: IAudioVolumeLevel (devicetopology.h)
description: The IAudioVolumeLevel interface provides access to a hardware volume control.
helpviewer_keywords: ["IAudioVolumeLevel","IAudioVolumeLevel interface [Core Audio]","IAudioVolumeLevel interface [Core Audio]","described","coreaudio.iaudiovolumelevel","devicetopology/IAudioVolumeLevel"]
old-location: coreaudio\iaudiovolumelevel.htm
tech.root: CoreAudio
ms.assetid: 5e7d7111-e4b0-43b3-af35-9878d1a19e5f
ms.date: 12/05/2018
ms.keywords: IAudioVolumeLevel, IAudioVolumeLevel interface [Core Audio], IAudioVolumeLevel interface [Core Audio],described, coreaudio.iaudiovolumelevel, devicetopology/IAudioVolumeLevel
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IAudioVolumeLevel
 - devicetopology/IAudioVolumeLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioVolumeLevel
---

# IAudioVolumeLevel interface


## -description

The <b>IAudioVolumeLevel</b> interface provides access to a hardware volume control. The client obtains a reference to the <b>IAudioVolumeLevel</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioVolumeLevel. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioVolumeLevel</b> interface. Only a subunit object that represents a hardware volume-level control will support this interface.



The <b>IAudioVolumeLevel</b> interface provides per-channel controls for setting and getting the gain or attenuation levels in the audio stream. If a volume-level hardware control can only attenuate the channels in the audio stream, then the maximum volume level for any channel is 0 dB. If a volume-level control can provide gain (amplification), then the maximum volume level is greater than 0 dB.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioVolumeLevel</b> interface provides convenient access to the KSPROPERTY_AUDIO_VOLUMELEVEL property of a subunit that has a subtype GUID value of KSNODETYPE_VOLUME. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>