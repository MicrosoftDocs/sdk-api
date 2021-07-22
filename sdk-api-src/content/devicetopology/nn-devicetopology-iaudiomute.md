---
UID: NN:devicetopology.IAudioMute
title: IAudioMute (devicetopology.h)
description: The IAudioMute interface provides access to a hardware mute control.
helpviewer_keywords: ["IAudioMute","IAudioMute interface [Core Audio]","IAudioMute interface [Core Audio]","described","coreaudio.iaudiomute","devicetopology/IAudioMute"]
old-location: coreaudio\iaudiomute.htm
tech.root: CoreAudio
ms.assetid: 53d49af7-81c3-4e75-ba06-dcee34d84292
ms.date: 12/05/2018
ms.keywords: IAudioMute, IAudioMute interface [Core Audio], IAudioMute interface [Core Audio],described, coreaudio.iaudiomute, devicetopology/IAudioMute
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
 - IAudioMute
 - devicetopology/IAudioMute
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
 - IAudioMute
---

# IAudioMute interface


## -description

The <b>IAudioMute</b> interface provides access to a hardware mute control. The client obtains a reference to the <b>IAudioMute</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioMute. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioMute</b> interface. Only a subunit object that represents a hardware mute control function will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioMute</b> interface provides convenient access to the KSPROPERTY_AUDIO_MUTE property of a subunit that has a subtype GUID value of KSNODETYPE_MUTE. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -inheritance

The <b>IAudioMute</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioMute</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
