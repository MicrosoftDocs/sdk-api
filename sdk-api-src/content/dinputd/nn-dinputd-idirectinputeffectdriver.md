---
UID: NN:dinputd.IDirectInputEffectDriver
title: IDirectInputEffectDriver (dinputd.h)
author: windows-sdk-content
description: These three methods allow additional interfaces to be added to the DirectInputEffectDriver object without affecting the functionality of the original interface.
old-location: hid\idirectinputeffectdriver.htm
tech.root: hid
ms.assetid: 8071dcc8-21e3-4157-827c-18e4f2abf303
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectInputEffectDriver, IDirectInputEffectDriver interface [Human Input Devices], IDirectInputEffectDriver interface [Human Input Devices],described, di_ref_298f3a98-21fc-407e-8a6a-a50249fe6a12.xml, dinputd/IDirectInputEffectDriver, hid.idirectinputeffectdriver
ms.topic: interface
f1_keywords: ["dinputd/IDirectInputEffectDriver"]
req.header: dinputd.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dinputd.h
api_name:
 - IDirectInputEffectDriver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectInputEffectDriver interface


## -description


These three methods allow additional interfaces to be added to the DirectInputEffectDriver object without affecting the functionality of the original interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectInputEffectDriver</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectInputEffectDriver</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-addref">IDirectInputEffectDriver::AddRef</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::AddRef </b>method increases the reference count of the DirectInputEffectDriver object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-destroyeffect">IDirectInputEffectDriver::DestroyEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::DestroyEffect </b>method removes an effect from the device. If the effect is playing, the driver should stop it before unloading it. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-deviceid">IDirectInputEffectDriver::DeviceID</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::DeviceID </b>method sends the driver the identity of the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-downloadeffect">IDirectInputEffectDriver::DownloadEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::DownloadEffect</b> method sends an effect to the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-escape">IDirectInputEffectDriver::Escape</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::Escape </b>method escapes to the driver. This method is called in response to an application invoking the <b>IDirectInputEffect::Escape</b> or <b>IDirectInputDevice::Escape</b> methods. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-geteffectstatus">IDirectInputEffectDriver::GetEffectStatus</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::GetEffectStatus </b>method obtains information about the status of an effect. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-getforcefeedbackstate">IDirectInputEffectDriver::GetForceFeedbackState</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::GetForceFeedbackState </b>method retrieves the force-feedback state for the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-getversions">IDirectInputEffectDriver::GetVersions</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::GetVersions </b>method obtains version information about the force-feedback hardware and driver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-queryinterface">IDirectInputEffectDriver::QueryInterface</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::QueryInterface </b>method determines whether the DirectInputEffectDriver object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-release">IDirectInputEffectDriver::Release</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::Release </b>method decreases the reference count of the DirectInputEffectDriver object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputEffectDriver. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-sendforcefeedbackcommand">IDirectInputEffectDriver::SendForceFeedbackCommand</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::SendForceFeedbackCommand </b>method changes the force-feedback state for the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-setgain">IDirectInputEffectDriver::SetGain</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::SetGain </b>method sets the overall device gain. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-starteffect">IDirectInputEffectDriver::StartEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::StartEffect</b> method begins the playback of an effect. If the effect is already playing, it is restarted from the beginning. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dinputd/nf-dinputd-idirectinputeffectdriver-stopeffect">IDirectInputEffectDriver::StopEffect</a>
</td>
<td align="left" width="63%">
The <b>IDirectInputEffectDriver::StopEffect </b>method halts the playback of an effect. 

</td>
</tr>
</table> 

