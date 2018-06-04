---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectInputEffectDriver interface


## -description


These three methods allow additional interfaces to be added to the DirectInputEffectDriver object without affecting the functionality of the original interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectInputEffectDriver</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectInputEffectDriver</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectInputEffectDriver</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540057">IDirectInputEffectDriver::AddRef</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::AddRef </b>method increases the reference count of the DirectInputEffectDriver object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540061">IDirectInputEffectDriver::DestroyEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::DestroyEffect </b>method removes an effect from the device. If the effect is playing, the driver should stop it before unloading it. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540072">IDirectInputEffectDriver::DeviceID</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::DeviceID </b>method sends the driver the identity of the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540078">IDirectInputEffectDriver::DownloadEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::DownloadEffect</b> method sends an effect to the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540081">IDirectInputEffectDriver::Escape</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::Escape </b>method escapes to the driver. This method is called in response to an application invoking the <b>IDirectInputEffect::Escape</b> or <b>IDirectInputDevice::Escape</b> methods. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540091">IDirectInputEffectDriver::GetEffectStatus</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::GetEffectStatus </b>method obtains information about the status of an effect. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540099">IDirectInputEffectDriver::GetForceFeedbackState</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::GetForceFeedbackState </b>method retrieves the force-feedback state for the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540104">IDirectInputEffectDriver::GetVersions</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::GetVersions </b>method obtains version information about the force-feedback hardware and driver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540112">IDirectInputEffectDriver::QueryInterface</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::QueryInterface </b>method determines whether the DirectInputEffectDriver object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540960">IDirectInputEffectDriver::Release</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::Release </b>method decreases the reference count of the DirectInputEffectDriver object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540961">IDirectInputEffectDriver::SendForceFeedbackCommand</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::SendForceFeedbackCommand </b>method changes the force-feedback state for the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540964">IDirectInputEffectDriver::SetGain</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::SetGain </b>method sets the overall device gain. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540966">IDirectInputEffectDriver::StartEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::StartEffect</b> method begins the playback of an effect. If the effect is already playing, it is restarted from the beginning. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540970">IDirectInputEffectDriver::StopEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::StopEffect </b>method halts the playback of an effect. 

</td>
</tr>
</table> 

