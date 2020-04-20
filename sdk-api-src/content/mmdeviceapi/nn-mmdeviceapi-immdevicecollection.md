---
UID: NN:mmdeviceapi.IMMDeviceCollection
title: IMMDeviceCollection (mmdeviceapi.h)
description: The IMMDeviceCollection interface represents a collection of multimedia device resources.helpviewer_keywords: ["IMMDeviceCollection","IMMDeviceCollection interface [Core Audio]","IMMDeviceCollection interface [Core Audio]","described","coreaudio.immdevicecollection","mmdeviceapi/IMMDeviceCollection"]
old-location: coreaudio\immdevicecollection.htm
tech.root: CoreAudio
ms.assetid: 4769b0a6-a319-4605-8742-5e7c285679cf
ms.date: 12/05/2018
ms.keywords: IMMDeviceCollection, IMMDeviceCollection interface [Core Audio], IMMDeviceCollection interface [Core Audio],described, coreaudio.immdevicecollection, mmdeviceapi/IMMDeviceCollection
f1_keywords:
- mmdeviceapi/IMMDeviceCollection
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
- IMMDeviceCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMMDeviceCollection interface


## -description



The <b>IMMDeviceCollection</b> interface represents a collection of multimedia device resources. In the current implementation, the only device resources that the MMDevice API can create collections of are <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint devices</a>.

A client can obtain a reference to an <b>IMMDeviceCollection</b> interface instance by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a> method. This method creates a collection of endpoint objects, each of which represents an audio endpoint device in the system. Each endpoint object in the collection supports the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint</a> interfaces. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>.

For a code example that uses the <b>IMMDeviceCollection</b> interface, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-properties">Device Properties</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMDeviceCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMDeviceCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMMDeviceCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of the devices in the device collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the specified item in the device collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator">IMMDeviceEnumerator Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint">IMMEndpoint Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
 

 

