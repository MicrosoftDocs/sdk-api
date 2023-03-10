---
UID: NN:devicetopology.IAudioOutputSelector
title: IAudioOutputSelector (devicetopology.h)
description: The IAudioOutputSelector interface provides access to a hardware demultiplexer control (output selector).
helpviewer_keywords: ["IAudioOutputSelector","IAudioOutputSelector interface [Core Audio]","IAudioOutputSelector interface [Core Audio]","described","coreaudio.iaudiooutputselector","devicetopology/IAudioOutputSelector"]
old-location: coreaudio\iaudiooutputselector.htm
tech.root: CoreAudio
ms.assetid: 571a44b6-972f-4d75-a31f-0e02cf728764
ms.date: 12/05/2018
ms.keywords: IAudioOutputSelector, IAudioOutputSelector interface [Core Audio], IAudioOutputSelector interface [Core Audio],described, coreaudio.iaudiooutputselector, devicetopology/IAudioOutputSelector
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
 - IAudioOutputSelector
 - devicetopology/IAudioOutputSelector
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
 - IAudioOutputSelector
---

# IAudioOutputSelector interface


## -description

The <b>IAudioOutputSelector</b> interface provides access to a hardware demultiplexer control (output selector). The client obtains a reference to the <b>IAudioOutputSelector</b> interface of a subunit by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioOutputSelector. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioOutputSelector</b> interface. Only a subunit object that represents a hardware output selector will support this interface.

Each output of an output selector is identified by the local ID of the part (a connector or subunit of a device topology) with a direct link to the output. A local ID is a number that uniquely identifies a part among all the parts in a device topology.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioOutputSelector</b> interface provides convenient access to the KSPROPERTY_AUDIO_DEMUX_DEST property of a subunit that has a subtype GUID value of KSNODETYPE_DEMUX. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -inheritance

The <b>IAudioOutputSelector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioOutputSelector</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
