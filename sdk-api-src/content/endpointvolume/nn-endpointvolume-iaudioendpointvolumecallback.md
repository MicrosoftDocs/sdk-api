---
UID: NN:endpointvolume.IAudioEndpointVolumeCallback
title: IAudioEndpointVolumeCallback
author: windows-driver-content
description: The IAudioEndpointVolumeCallback interface provides notifications of changes in the volume level and muting state of an audio endpoint device.
old-location: coreaudio\iaudioendpointvolumecallback.htm
old-project: CoreAudio
ms.assetid: 0b631d1b-f89c-4789-a09c-875b24a48a89
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: IAudioEndpointVolumeCallback, IAudioEndpointVolumeCallback interface [Core Audio], IAudioEndpointVolumeCallback interface [Core Audio], described, coreaudio.iaudioendpointvolumecallback, endpointvolume/IAudioEndpointVolumeCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Endpointvolume.h
api_name:
-	IAudioEndpointVolumeCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioEndpointVolumeCallback interface


## -description



The <b>IAudioEndpointVolumeCallback</b> interface provides notifications of changes in the volume level and muting state of an audio endpoint device. Unlike the other interfaces in this section, which are implemented by the WASAPI system component, an EndpointVolume API client implements the <b>IAudioEndpointVolumeCallback</b> interface. To receive event notifications, the client passes a pointer to its <b>IAudioEndpointVolumeCallback</b> interface to the <a href="https://msdn.microsoft.com/0a5711fa-700a-44ae-beed-aec421365b4c">IAudioEndpointVolume::RegisterControlChangeNotify</a> method.

After registering its <b>IAudioEndpointVolumeCallback</b> interface, the client receives event notifications in the form of callbacks through the <b>OnNotify</b> method in the interface. These event notifications occur when one of the following methods causes a change in the volume level or muting state of an endpoint device:

<ul>
<li>
<a href="https://msdn.microsoft.com/51f3b4dd-be9d-4b83-8605-a9962c6709a3">IAudioEndpointVolume::SetChannelVolumeLevel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2e1f0d1c-060f-45b7-9194-591e45668b52">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>
</li>
<li>
<a href="https://msdn.microsoft.com/776d7667-f48b-44c0-9441-177b86b52da9">IAudioEndpointVolume::SetMasterVolumeLevel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d592c197-32fc-4a48-8f37-1cd140895c5e">IAudioEndpointVolume::SetMasterVolumeLevelScalar</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0ab4fef-8333-4f21-ae8e-74285788ae0e">IAudioEndpointVolume::SetMute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c334d780-784b-4fa3-bf4f-ea5d65459baf">IAudioEndpointVolume::VolumeStepDown</a>
</li>
<li>
<a href="https://msdn.microsoft.com/35ed44cd-ba91-4b6a-b528-0e22df389d31">IAudioEndpointVolume::VolumeStepUp</a>
</li>
</ul>
If an audio endpoint device implements hardware volume and mute controls, the <b>IAudioEndpointVolume</b> interface uses the hardware controls to manage the device's volume. Otherwise, the <b>IAudioEndpointVolume</b> interface implements volume and mute controls in software, transparently to the client.

If a device has hardware volume and mute controls, changes made to the volume and mute settings through the methods in the preceding list affect the device's volume in both shared mode and exclusive mode. If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through these methods affect the device's volume in shared mode, but not in exclusive mode. In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls. However, changes made to the software controls through these methods generate event notifications regardless of whether the device is operating in shared mode or in exclusive mode. Changes made to the software volume and mute controls while the device operates in exclusive mode take effect when the device switches to shared mode.

To determine whether a device has hardware volume and mute controls, call the <a href="https://msdn.microsoft.com/20d04cff-f101-417e-912f-c87af16184db">IAudioEndpointVolume::QueryHardwareSupport</a> method.

In implementing the <b>IAudioEndpointVolumeCallback</b> interface, the client should observe these rules to avoid deadlocks:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="https://msdn.microsoft.com/4ae8263b-83f5-4d9f-9e48-d78fae98c7ad">IAudioEndpointVolume::UnregisterControlChangeNotify</a> method during an event callback.</li>
<li>The client should never release the final reference on an EndpointVolume API object during an event callback.</li>
</ul>
For a code example that implements the <b>IAudioEndpointVolumeCallback</b> interface, see <a href="https://msdn.microsoft.com/667c3659-69ae-469d-9ae0-e32a189cbc71">Endpoint Volume Controls</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointVolumeCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpointVolumeCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointVolumeCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">OnNotify</a>
</td>
<td align="left" width="63%">
Notifies the client that the volume level or muting state of the audio endpoint device has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79">EndpointVolume API</a>



<a href="https://msdn.microsoft.com/0a5711fa-700a-44ae-beed-aec421365b4c">IAudioEndpointVolume::RegisterControlChangeNotify</a>



<a href="https://msdn.microsoft.com/4ae8263b-83f5-4d9f-9e48-d78fae98c7ad">IAudioEndpointVolume::UnregisterControlChangeNotify</a>
 

 

