---
UID: NN:devicetopology.IAudioChannelConfig
title: IAudioChannelConfig (devicetopology.h)
description: The IAudioChannelConfig interface provides access to a hardware channel-configuration control.
helpviewer_keywords: ["IAudioChannelConfig","IAudioChannelConfig interface [Core Audio]","IAudioChannelConfig interface [Core Audio]","described","coreaudio.iaudiochannelconfig","devicetopology/IAudioChannelConfig"]
old-location: coreaudio\iaudiochannelconfig.htm
tech.root: CoreAudio
ms.assetid: b8e54e9e-a6eb-46e6-a71c-ff498c7e8f47
ms.date: 12/05/2018
ms.keywords: IAudioChannelConfig, IAudioChannelConfig interface [Core Audio], IAudioChannelConfig interface [Core Audio],described, coreaudio.iaudiochannelconfig, devicetopology/IAudioChannelConfig
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
 - IAudioChannelConfig
 - devicetopology/IAudioChannelConfig
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
 - IAudioChannelConfig
---

# IAudioChannelConfig interface


## -description

The <b>IAudioChannelConfig</b> interface provides access to a hardware channel-configuration control. The client obtains a reference to the <b>IAudioChannelConfig</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioChannelConfig. The call to IPart::Activate succeeds only if the subunit supports the <b>IAudioChannelConfig</b> interface. Only a subunit object that represents a hardware channel-configuration control will support this interface.

A client of the <b>IAudioChannelConfig</b> interface programs a hardware channel-configuration control by writing a channel-configuration mask to the control. The mask specifies the assignment of audio channels to speakers. For more information about channel-configuration masks, see [KSPROPERTY_AUDIO_CHANNEL_CONFIG](/windows-hardware/drivers/audio/ksproperty-audio-channel-config).

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioChannelConfig</b> interface provides convenient access to the KSPROPERTY_AUDIO_CHANNEL_CONFIG property of a subunit that has a subtype GUID value of KSNODETYPE_3D_EFFECTS, KSNODETYPE_DAC, KSNODETYPE_VOLUME, or KSNODETYPE_PROLOGIC_DECODER. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -inheritance

The <b>IAudioChannelConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioChannelConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
