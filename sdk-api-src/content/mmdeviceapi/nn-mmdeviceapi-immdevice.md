---
UID: NN:mmdeviceapi.IMMDevice
title: IMMDevice (mmdeviceapi.h)
author: windows-sdk-content
description: The IMMDevice interface encapsulates the generic features of a multimedia device resource.
old-location: coreaudio\immdevice.htm
tech.root: CoreAudio
ms.assetid: 12b05e7e-81b2-49fd-bb9f-d5ad3315c580
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMMDevice, IMMDevice interface [Core Audio], IMMDevice interface [Core Audio],described, coreaudio.immdevice, mmdeviceapi/IMMDevice
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMMDevice interface


## -description



The <b>IMMDevice</b> interface encapsulates the generic features of a multimedia device resource. In the current implementation of the MMDevice API, the only type of device resource that an <b>IMMDevice</b> interface can represent is an <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint device</a>.

A client can obtain an <b>IMMDevice</b> interface from one of the following methods:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>
</li>
</ul>
For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>.

After obtaining the <b>IMMDevice</b> interface of an audio endpoint device, a client can obtain an interface that encapsulates the endpoint-specific features of the device by calling the <b>IMMDevice::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IMMEndpoint. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>.

For code examples that use the <b>IMMDevice</b> interface, see the following topics:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-roles-for-legacy-windows-multimedia-applications">Device Roles for Legacy Windows Multimedia Applications</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMMDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">Activate</a>
</td>
<td align="left" width="63%">
Creates a COM object with the specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid">GetId</a>
</td>
<td align="left" width="63%">
Gets a string that identifies the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getstate">GetState</a>
</td>
<td align="left" width="63%">
Gets the current state of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore">OpenPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an interface to the device's property store.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">IMMDeviceEnumerator::GetDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
 

 

