---
UID: NN:devicetopology.IAudioPeakMeter
title: IAudioPeakMeter (devicetopology.h)
description: The IAudioPeakMeter interface provides access to a hardware peak-meter control.
helpviewer_keywords: ["IAudioPeakMeter","IAudioPeakMeter interface [Core Audio]","IAudioPeakMeter interface [Core Audio]","described","coreaudio.iaudiopeakmeter","devicetopology/IAudioPeakMeter"]
old-location: coreaudio\iaudiopeakmeter.htm
tech.root: CoreAudio
ms.assetid: 524d83ff-4303-448c-a070-58d17dec03ba
ms.date: 12/05/2018
ms.keywords: IAudioPeakMeter, IAudioPeakMeter interface [Core Audio], IAudioPeakMeter interface [Core Audio],described, coreaudio.iaudiopeakmeter, devicetopology/IAudioPeakMeter
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
 - IAudioPeakMeter
 - devicetopology/IAudioPeakMeter
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
 - IAudioPeakMeter
---

# IAudioPeakMeter interface


## -description

The <b>IAudioPeakMeter</b> interface provides access to a hardware peak-meter control. The client obtains a reference to the <b>IAudioPeakMeter</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioPeakMeter. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioPeakMeter</b> interface. Only a subunit object that represents a hardware peak meter will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioPeakMeter</b> interface provides convenient access to the KSPROPERTY_AUDIO_PEAKMETER property of a subunit that has a subtype GUID value of KSNODETYPE_PEAKMETER. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -inheritance

The <b>IAudioPeakMeter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioPeakMeter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
