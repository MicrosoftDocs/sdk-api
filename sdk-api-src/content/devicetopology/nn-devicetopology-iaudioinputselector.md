---
UID: NN:devicetopology.IAudioInputSelector
title: IAudioInputSelector (devicetopology.h)
description: The IAudioInputSelector interface provides access to a hardware multiplexer control (input selector).
helpviewer_keywords: ["IAudioInputSelector","IAudioInputSelector interface [Core Audio]","IAudioInputSelector interface [Core Audio]","described","coreaudio.iaudioinputselector","devicetopology/IAudioInputSelector"]
old-location: coreaudio\iaudioinputselector.htm
tech.root: CoreAudio
ms.assetid: 6f5ce9c0-39e4-4fab-910c-9a11b90fcde7
ms.date: 12/05/2018
ms.keywords: IAudioInputSelector, IAudioInputSelector interface [Core Audio], IAudioInputSelector interface [Core Audio],described, coreaudio.iaudioinputselector, devicetopology/IAudioInputSelector
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
 - IAudioInputSelector
 - devicetopology/IAudioInputSelector
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
 - IAudioInputSelector
---

# IAudioInputSelector interface


## -description

The <b>IAudioInputSelector</b> interface provides access to a hardware multiplexer control (input selector). The client obtains a reference to the <b>IAudioInputSelector</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioInputSelector. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioInputSelector</b> interface. Only a subunit object that represents a hardware input selector will support this interface.

Each input of an input selector is identified by the local ID of the part (a connector or subunit of a device topology) that has a direct link to the input. A local ID is a number that uniquely identifies a part among all the parts in a device topology.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioInputSelector</b> interface provides convenient access to the KSPROPERTY_AUDIO_MUX_SOURCE property of a subunit that has a subtype GUID value of KSNODETYPE_MUX. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

For a code example that uses the <b>IAudioInputSelector</b> interface, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -inheritance

The <b>IAudioInputSelector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioInputSelector</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
