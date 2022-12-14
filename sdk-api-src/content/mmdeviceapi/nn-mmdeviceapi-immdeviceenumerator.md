---
UID: NN:mmdeviceapi.IMMDeviceEnumerator
title: IMMDeviceEnumerator (mmdeviceapi.h)
description: The IMMDeviceEnumerator interface provides methods for enumerating multimedia device resources.
helpviewer_keywords: ["IMMDeviceEnumerator","IMMDeviceEnumerator interface [Core Audio]","IMMDeviceEnumerator interface [Core Audio]","described","coreaudio.immdeviceenumerator","mmdeviceapi/IMMDeviceEnumerator"]
old-location: coreaudio\immdeviceenumerator.htm
tech.root: CoreAudio
ms.assetid: 1abdeac1-c156-40b8-8b8c-5ddb51e410aa
ms.date: 12/05/2018
ms.keywords: IMMDeviceEnumerator, IMMDeviceEnumerator interface [Core Audio], IMMDeviceEnumerator interface [Core Audio],described, coreaudio.immdeviceenumerator, mmdeviceapi/IMMDeviceEnumerator
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
 - IMMDeviceEnumerator
 - mmdeviceapi/IMMDeviceEnumerator
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
 - IMMDeviceEnumerator
---

# IMMDeviceEnumerator interface


## -description

The <b>IMMDeviceEnumerator</b> interface provides methods for enumerating multimedia device resources. In the current implementation of the MMDevice API, the only device resources that this interface can enumerate are <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint devices</a>. A client obtains a reference to an <b>IMMDeviceEnumerator</b> interface by calling the <b>CoCreateInstance</b> function, as described previously (see <a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>).

The device resources enumerated by the methods in the <b>IMMDeviceEnumerator</b> interface are represented as collections of objects with <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interfaces. A collection has an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection</a> interface. The <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a> method creates a device collection.

To obtain a pointer to the <b>IMMDevice</b> interface of an item in a device collection, the client calls the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a> method.

For code examples that use the <b>IMMDeviceEnumerator</b> interface, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
</ul>

## -inheritance

The <b>IMMDeviceEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMDeviceEnumerator</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
