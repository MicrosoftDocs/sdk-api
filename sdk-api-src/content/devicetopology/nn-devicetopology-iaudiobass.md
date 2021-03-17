---
UID: NN:devicetopology.IAudioBass
title: IAudioBass (devicetopology.h)
description: The IAudioBass interface provides access to a hardware bass-level control.
helpviewer_keywords: ["IAudioBass","IAudioBass interface [Core Audio]","IAudioBass interface [Core Audio]","described","coreaudio.iaudiobass","devicetopology/IAudioBass"]
old-location: coreaudio\iaudiobass.htm
tech.root: CoreAudio
ms.assetid: 036ca996-8612-4905-9afa-a4c3b4624652
ms.date: 12/05/2018
ms.keywords: IAudioBass, IAudioBass interface [Core Audio], IAudioBass interface [Core Audio],described, coreaudio.iaudiobass, devicetopology/IAudioBass
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
 - IAudioBass
 - devicetopology/IAudioBass
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
 - IAudioBass
---

# IAudioBass interface


## -description

The <b>IAudioBass</b> interface provides access to a hardware bass-level control. The client obtains a reference to the <b>IAudioBass</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioBass. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioBass</b> interface. Only a subunit object that represents a hardware function for controlling the level of the bass frequencies in each channel will support this interface.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>