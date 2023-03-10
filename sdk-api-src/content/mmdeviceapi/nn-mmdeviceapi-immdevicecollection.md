---
UID: NN:mmdeviceapi.IMMDeviceCollection
title: IMMDeviceCollection (mmdeviceapi.h)
description: The IMMDeviceCollection interface represents a collection of multimedia device resources.
helpviewer_keywords: ["IMMDeviceCollection","IMMDeviceCollection interface [Core Audio]","IMMDeviceCollection interface [Core Audio]","described","coreaudio.immdevicecollection","mmdeviceapi/IMMDeviceCollection"]
old-location: coreaudio\immdevicecollection.htm
tech.root: CoreAudio
ms.assetid: 4769b0a6-a319-4605-8742-5e7c285679cf
ms.date: 12/05/2018
ms.keywords: IMMDeviceCollection, IMMDeviceCollection interface [Core Audio], IMMDeviceCollection interface [Core Audio],described, coreaudio.immdevicecollection, mmdeviceapi/IMMDeviceCollection
req.header: mmdeviceapi.h
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
 - IMMDeviceCollection
 - mmdeviceapi/IMMDeviceCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDeviceCollection
---

# IMMDeviceCollection interface


## -description

The <b>IMMDeviceCollection</b> interface represents a collection of multimedia device resources. In the current implementation, the only device resources that the MMDevice API can create collections of are <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint devices</a>.

A client can obtain a reference to an <b>IMMDeviceCollection</b> interface instance by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a> method. This method creates a collection of endpoint objects, each of which represents an audio endpoint device in the system. Each endpoint object in the collection supports the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint</a> interfaces. For more information, see <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>.

For a code example that uses the <b>IMMDeviceCollection</b> interface, see <a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>.

## -inheritance

The <b>IMMDeviceCollection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMDeviceCollection</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>



<a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
