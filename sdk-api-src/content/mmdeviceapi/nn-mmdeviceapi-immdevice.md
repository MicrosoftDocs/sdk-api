---
UID: NN:mmdeviceapi.IMMDevice
title: IMMDevice (mmdeviceapi.h)
description: The IMMDevice interface encapsulates the generic features of a multimedia device resource.
helpviewer_keywords: ["IMMDevice","IMMDevice interface [Core Audio]","IMMDevice interface [Core Audio]","described","coreaudio.immdevice","mmdeviceapi/IMMDevice"]
old-location: coreaudio\immdevice.htm
tech.root: CoreAudio
ms.assetid: 12b05e7e-81b2-49fd-bb9f-d5ad3315c580
ms.date: 12/05/2018
ms.keywords: IMMDevice, IMMDevice interface [Core Audio], IMMDevice interface [Core Audio],described, coreaudio.immdevice, mmdeviceapi/IMMDevice
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
 - IMMDevice
 - mmdeviceapi/IMMDevice
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
 - IMMDevice
---

# IMMDevice interface


## -description

The <b>IMMDevice</b> interface encapsulates the generic features of a multimedia device resource. In the current implementation of the MMDevice API, the only type of device resource that an <b>IMMDevice</b> interface can represent is an <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint device</a>.

A client can obtain an <b>IMMDevice</b> interface from one of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a>
</li>
<li>
<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>
</li>
<li>
<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>
</li>
</ul>
For more information, see <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>.

After obtaining the <b>IMMDevice</b> interface of an audio endpoint device, a client can obtain an interface that encapsulates the endpoint-specific features of the device by calling the <b>IMMDevice::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IMMEndpoint. For more information, see <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>.

For code examples that use the <b>IMMDevice</b> interface, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/device-roles-for-legacy-windows-multimedia-applications">Device Roles for Legacy Windows Multimedia Applications</a>
</li>
</ul>

## -inheritance

The <b>IMMDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMDevice</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>



<a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
