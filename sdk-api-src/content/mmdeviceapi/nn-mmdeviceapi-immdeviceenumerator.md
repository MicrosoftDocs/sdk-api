---
UID: NN:mmdeviceapi.IMMDeviceEnumerator
title: IMMDeviceEnumerator
author: windows-sdk-content
description: The IMMDeviceEnumerator interface provides methods for enumerating multimedia device resources.
old-location: coreaudio\immdeviceenumerator.htm
tech.root: CoreAudio
ms.assetid: 1abdeac1-c156-40b8-8b8c-5ddb51e410aa
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IMMDeviceEnumerator, IMMDeviceEnumerator interface [Core Audio], IMMDeviceEnumerator interface [Core Audio],described, coreaudio.immdeviceenumerator, mmdeviceapi/IMMDeviceEnumerator
ms.prod: windows
ms.technology: windows-sdk
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
 - IMMDeviceEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMDeviceEnumerator interface


## -description



The <b>IMMDeviceEnumerator</b> interface provides methods for enumerating multimedia device resources. In the current implementation of the MMDevice API, the only device resources that this interface can enumerate are <a href="https://msdn.microsoft.com/773714fb-3b00-4f03-988f-05c5835f87cf">audio endpoint devices</a>. A client obtains a reference to an <b>IMMDeviceEnumerator</b> interface by calling the <b>CoCreateInstance</b> function, as described previously (see <a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">MMDevice API</a>).

The device resources enumerated by the methods in the <b>IMMDeviceEnumerator</b> interface are represented as collections of objects with <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interfaces. A collection has an <a href="https://msdn.microsoft.com/4769b0a6-a319-4605-8742-5e7c285679cf">IMMDeviceCollection</a> interface. The <a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a> method creates a device collection.

To obtain a pointer to the <b>IMMDevice</b> interface of an item in a device collection, the client calls the <a href="https://msdn.microsoft.com/98cb72fd-9422-44b4-a585-a1fed029a77f">IMMDeviceCollection::Item</a> method.

For code examples that use the <b>IMMDeviceEnumerator</b> interface, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/ad8753ba-ad20-4122-b0f2-eb165f98db67">Device Properties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMDeviceEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMMDeviceEnumerator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">EnumAudioEndpoints</a>
</td>
<td align="left" width="63%">
Generates a collection of audio endpoint devices that meet the specified criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">GetDefaultAudioEndpoint</a>
</td>
<td align="left" width="63%">
Retrieves the default audio endpoint for the specified data-flow direction and role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves an endpoint device that is specified by an endpoint device-identification string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">RegisterEndpointNotificationCallback</a>
</td>
<td align="left" width="63%">
Registers a client's notification callback interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc1e85af-f399-469d-806a-a2d80b700b75">UnregisterEndpointNotificationCallback</a>
</td>
<td align="left" width="63%">
Deletes the registration of a notification interface that the client registered in a previous call to the <a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/4769b0a6-a319-4605-8742-5e7c285679cf">IMMDeviceCollection Interface</a>



<a href="https://msdn.microsoft.com/98cb72fd-9422-44b4-a585-a1fed029a77f">IMMDeviceCollection::Item</a>



<a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a>



<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">MMDevice API</a>
 

 

