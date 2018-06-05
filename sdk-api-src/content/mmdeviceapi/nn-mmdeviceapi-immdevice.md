---
UID: NN:mmdeviceapi.IMMDevice
title: IMMDevice
author: windows-sdk-content
description: The IMMDevice interface encapsulates the generic features of a multimedia device resource.
old-location: coreaudio\immdevice.htm
old-project: CoreAudio
ms.assetid: 12b05e7e-81b2-49fd-bb9f-d5ad3315c580
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IMMDevice, IMMDevice interface [Core Audio], IMMDevice interface [Core Audio],described, coreaudio.immdevice, mmdeviceapi/IMMDevice
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
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mmdeviceapi.h
api_name:
-	IMMDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmdevapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMMDevice interface


## -description



The <b>IMMDevice</b> interface encapsulates the generic features of a multimedia device resource. In the current implementation of the MMDevice API, the only type of device resource that an <b>IMMDevice</b> interface can represent is an <a href="https://msdn.microsoft.com/773714fb-3b00-4f03-988f-05c5835f87cf">audio endpoint device</a>.

A client can obtain an <b>IMMDevice</b> interface from one of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/98cb72fd-9422-44b4-a585-a1fed029a77f">IMMDeviceCollection::Item</a>
</li>
<li>
<a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a>
</li>
</ul>
For more information, see <a href="https://msdn.microsoft.com/4769b0a6-a319-4605-8742-5e7c285679cf">IMMDeviceCollection Interface</a>.

After obtaining the <b>IMMDevice</b> interface of an audio endpoint device, a client can obtain an interface that encapsulates the endpoint-specific features of the device by calling the <b>IMMDevice::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IMMEndpoint. For more information, see <a href="https://msdn.microsoft.com/293de8eb-204a-4c18-807c-b1405db85b12">IMMEndpoint Interface</a>.

For code examples that use the <b>IMMDevice</b> interface, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/ad8753ba-ad20-4122-b0f2-eb165f98db67">Device Properties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/54dcaa0e-2652-406d-ba24-c8885924acc6">Device Roles for Legacy Windows Multimedia Applications</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMMDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">Activate</a>
</td>
<td align="left" width="63%">
Creates a COM object with the specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetId</a>
</td>
<td align="left" width="63%">
Gets a string that identifies the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b50773b-241c-4a32-8ab6-85adb3f885e1">GetState</a>
</td>
<td align="left" width="63%">
Gets the current state of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d13a5743-8b07-4876-ab9d-7a6bd60e7add">OpenPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an interface to the device's property store.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/4769b0a6-a319-4605-8742-5e7c285679cf">IMMDeviceCollection Interface</a>



<a href="https://msdn.microsoft.com/98cb72fd-9422-44b4-a585-a1fed029a77f">IMMDeviceCollection::Item</a>



<a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>



<a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a>



<a href="https://msdn.microsoft.com/293de8eb-204a-4c18-807c-b1405db85b12">IMMEndpoint Interface</a>



<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">MMDevice API</a>
 

 

