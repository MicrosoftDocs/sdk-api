---
UID: NN:mmdeviceapi.IMMDeviceEnumerator
title: IMMDeviceEnumerator (mmdeviceapi.h)
description: The IMMDeviceEnumerator interface provides methods for enumerating multimedia device resources.
old-location: coreaudio\immdeviceenumerator.htm
tech.root: CoreAudio
ms.assetid: 1abdeac1-c156-40b8-8b8c-5ddb51e410aa
ms.date: 12/05/2018
ms.keywords: IMMDeviceEnumerator, IMMDeviceEnumerator interface [Core Audio], IMMDeviceEnumerator interface [Core Audio],described, coreaudio.immdeviceenumerator, mmdeviceapi/IMMDeviceEnumerator
f1_keywords:
- mmdeviceapi/IMMDeviceEnumerator
dev_langs:
- c++
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
- IMMDeviceEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMMDeviceEnumerator interface


## -description



The <b>IMMDeviceEnumerator</b> interface provides methods for enumerating multimedia device resources. In the current implementation of the MMDevice API, the only device resources that this interface can enumerate are <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint devices</a>. A client obtains a reference to an <b>IMMDeviceEnumerator</b> interface by calling the <b>CoCreateInstance</b> function, as described previously (see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>).

The device resources enumerated by the methods in the <b>IMMDeviceEnumerator</b> interface are represented as collections of objects with <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interfaces. A collection has an <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection</a> interface. The <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a> method creates a device collection.

To obtain a pointer to the <b>IMMDevice</b> interface of an item in a device collection, the client calls the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a> method.

For code examples that use the <b>IMMDeviceEnumerator</b> interface, see the following topics:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-properties">Device Properties</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMDeviceEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMDeviceEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMMDeviceEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">EnumAudioEndpoints</a>
</td>
<td align="left" width="63%">
Generates a collection of audio endpoint devices that meet the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint">GetDefaultAudioEndpoint</a>
</td>
<td align="left" width="63%">
Retrieves the default audio endpoint for the specified data-flow direction and role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves an endpoint device that is specified by an endpoint device-identification string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">RegisterEndpointNotificationCallback</a>
</td>
<td align="left" width="63%">
Registers a client's notification callback interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback">UnregisterEndpointNotificationCallback</a>
</td>
<td align="left" width="63%">
Deletes the registration of a notification interface that the client registered in a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">IMMDeviceCollection::Item</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
 

 

