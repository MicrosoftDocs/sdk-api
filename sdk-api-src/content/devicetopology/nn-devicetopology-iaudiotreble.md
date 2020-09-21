---
UID: NN:devicetopology.IAudioTreble
title: IAudioTreble (devicetopology.h)
description: The IAudioTreble interface provides access to a hardware treble-level control.
helpviewer_keywords: ["IAudioTreble","IAudioTreble interface [Core Audio]","IAudioTreble interface [Core Audio]","described","coreaudio.iaudiotreble","devicetopology/IAudioTreble"]
old-location: coreaudio\iaudiotreble.htm
tech.root: CoreAudio
ms.assetid: 3ace174e-c21c-41e7-9830-80d247d8437f
ms.date: 12/05/2018
ms.keywords: IAudioTreble, IAudioTreble interface [Core Audio], IAudioTreble interface [Core Audio],described, coreaudio.iaudiotreble, devicetopology/IAudioTreble
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
 - IAudioTreble
 - devicetopology/IAudioTreble
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
 - IAudioTreble
---

# IAudioTreble interface


## -description

The <b>IAudioTreble</b> interface provides access to a hardware treble-level control. The client obtains a reference to the <b>IAudioTreble</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioTreble. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioTreble</b> interface. Only a subunit object that represents a hardware function for controlling the level of the treble frequencies in each channel will support this interface.



The <b>IAudioTreble</b> interface provides per-channel controls for setting and getting the gain or attenuation level of the treble frequencies in the audio stream. If a treble-level hardware control can only attenuate the channels in the audio stream, then the maximum treble level for any channel is 0 dB. If a treble-level control can provide gain (amplification), then the maximum treble level is greater than 0 dB.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioTreble</b> interface provides convenient access to the KSPROPERTY_AUDIO_TREBLE property of a subunit that has a subtype GUID value of KSNODETYPE_TONE. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>