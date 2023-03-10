---
UID: NN:devicetopology.IAudioLoudness
title: IAudioLoudness (devicetopology.h)
description: The IAudioLoudness interface provides access to a &quot;loudness&quot; compensation control.
helpviewer_keywords: ["IAudioLoudness","IAudioLoudness interface [Core Audio]","IAudioLoudness interface [Core Audio]","described","coreaudio.iaudioloudness","devicetopology/IAudioLoudness"]
old-location: coreaudio\iaudioloudness.htm
tech.root: CoreAudio
ms.assetid: c182d6ae-c55b-4e3b-9639-7c2f2f7d826d
ms.date: 12/05/2018
ms.keywords: IAudioLoudness, IAudioLoudness interface [Core Audio], IAudioLoudness interface [Core Audio],described, coreaudio.iaudioloudness, devicetopology/IAudioLoudness
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
 - IAudioLoudness
 - devicetopology/IAudioLoudness
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
 - IAudioLoudness
---

# IAudioLoudness interface


## -description

The <b>IAudioLoudness</b> interface provides access to a "loudness" compensation control. The client obtains a reference to the <b>IAudioLoudness</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioLoudness. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioLoudness</b> interface. Only a subunit object that represents a hardware loudness control function will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioLoudness</b> interface provides convenient access to the KSPROPERTY_AUDIO_LOUDNESS property of a subunit that has a subtype GUID value of KSNODETYPE_LOUDNESS. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -inheritance

The <b>IAudioLoudness</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioLoudness</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
