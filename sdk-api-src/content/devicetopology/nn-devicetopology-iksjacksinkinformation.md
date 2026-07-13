---
UID: NN:devicetopology.IKsJackSinkInformation
title: IKsJackSinkInformation (devicetopology.h)
description: The IKsJackSinkInformation interface provides access to jack sink information if the jack is supported by the hardware.
helpviewer_keywords: ["IKsJackSinkInformation","IKsJackSinkInformation interface [Core Audio]","IKsJackSinkInformation interface [Core Audio]","described","coreaudio.iksjacksinkinformation","devicetopology/IKsJackSinkInformation"]
old-location: coreaudio\iksjacksinkinformation.htm
tech.root: CoreAudio
ms.assetid: 4116a912-5ff2-4fc0-96c6-61d1e62cd973
ms.date: 12/05/2018
ms.keywords: IKsJackSinkInformation, IKsJackSinkInformation interface [Core Audio], IKsJackSinkInformation interface [Core Audio],described, coreaudio.iksjacksinkinformation, devicetopology/IKsJackSinkInformation
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IKsJackSinkInformation
 - devicetopology/IKsJackSinkInformation
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
 - IKsJackSinkInformation
---

# IKsJackSinkInformation interface


## -description

The <b>IKsJackSinkInformation</b> interface provides access to jack sink information if the jack is supported by the hardware.

The client obtains a reference to the <b>IKsJackSinkInformation</b> interface by activating it on the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of a bridge pin connector on a KS filter device topology object. To activate the object, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter refiid set to REFIID <b>IID_IKsJackSinkInformation</b>. 

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsJackSinkInformation</b> interface provides convenient access to the <b>KSPROPERTY_JACK_SINK_INFO</b> property of a connector to an endpoint device. For more information about KS properties and KS pins, see the Windows DDK documentation.

## -inheritance

The <b>IKsJackSinkInformation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsJackSinkInformation</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription</a>
