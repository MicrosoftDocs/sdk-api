---
UID: NN:devicetopology.IPerChannelDbLevel
title: IPerChannelDbLevel (devicetopology.h)
description: The IPerChannelDbLevel interface represents a generic subunit control interface that provides per-channel control over the volume level, in decibels, of an audio stream or of a frequency band in an audio stream.
helpviewer_keywords: ["IPerChannelDbLevel","IPerChannelDbLevel interface [Core Audio]","IPerChannelDbLevel interface [Core Audio]","described","coreaudio.iperchanneldblevel","devicetopology/IPerChannelDbLevel"]
old-location: coreaudio\iperchanneldblevel.htm
tech.root: CoreAudio
ms.assetid: e70b4518-c9de-4426-b8e5-db80656699a9
ms.date: 12/05/2018
ms.keywords: IPerChannelDbLevel, IPerChannelDbLevel interface [Core Audio], IPerChannelDbLevel interface [Core Audio],described, coreaudio.iperchanneldblevel, devicetopology/IPerChannelDbLevel
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
 - IPerChannelDbLevel
 - devicetopology/IPerChannelDbLevel
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
 - IPerChannelDbLevel
---

# IPerChannelDbLevel interface


## -description

The <b>IPerChannelDbLevel</b> interface represents a generic subunit control interface that provides per-channel control over the volume level, in decibels, of an audio stream or of a frequency band in an audio stream. A positive volume level represents gain, and a negative value represents attenuation.

Clients do not call the methods in this interface directly. Instead, this interface serves as the base interface for the following interfaces, which clients do call directly:

<ul>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass Interface</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange Interface</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble Interface</a>
</li>
<li>
<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel Interface</a>
</li>
</ul>

## -inheritance

The <b>IPerChannelDbLevel</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPerChannelDbLevel</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiobass">IAudioBass Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomidrange">IAudioMidrange Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiotreble">IAudioTreble Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel Interface</a>
