---
UID: NN:mmdeviceapi.IMMDeviceCollection
title: IMMDeviceCollection
author: windows-sdk-content
description: The IMMDeviceCollection interface represents a collection of multimedia device resources.
old-location: coreaudio\immdevicecollection.htm
tech.root: CoreAudio
ms.assetid: 4769b0a6-a319-4605-8742-5e7c285679cf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMMDeviceCollection, IMMDeviceCollection interface [Core Audio], IMMDeviceCollection interface [Core Audio],described, coreaudio.immdevicecollection, mmdeviceapi/IMMDeviceCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMMDeviceCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMDeviceCollection interface


## -description



The <b>IMMDeviceCollection</b> interface represents a collection of multimedia device resources. In the current implementation, the only device resources that the MMDevice API can create collections of are <a href="https://msdn.microsoft.com/773714fb-3b00-4f03-988f-05c5835f87cf">audio endpoint devices</a>.

A client can obtain a reference to an <b>IMMDeviceCollection</b> interface instance by calling the <a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a> method. This method creates a collection of endpoint objects, each of which represents an audio endpoint device in the system. Each endpoint object in the collection supports the <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> and <a href="https://msdn.microsoft.com/293de8eb-204a-4c18-807c-b1405db85b12">IMMEndpoint</a> interfaces. For more information, see <a href="https://msdn.microsoft.com/1abdeac1-c156-40b8-8b8c-5ddb51e410aa">IMMDeviceEnumerator Interface</a>.

For a code example that uses the <b>IMMDeviceCollection</b> interface, see <a href="https://msdn.microsoft.com/ad8753ba-ad20-4122-b0f2-eb165f98db67">Device Properties</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMDeviceCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMMDeviceCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/236a611b-98ab-437c-9e36-8c8a7c32ffbc">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of the devices in the device collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98cb72fd-9422-44b4-a585-a1fed029a77f">Item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the specified item in the device collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/1abdeac1-c156-40b8-8b8c-5ddb51e410aa">IMMDeviceEnumerator Interface</a>



<a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="https://msdn.microsoft.com/293de8eb-204a-4c18-807c-b1405db85b12">IMMEndpoint Interface</a>



<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">MMDevice API</a>
 

 

