---
UID: NN:endpointvolume.IAudioEndpointVolumeCallback
title: IAudioEndpointVolumeCallback (endpointvolume.h)
description: The IAudioEndpointVolumeCallback interface provides notifications of changes in the volume level and muting state of an audio endpoint device.
helpviewer_keywords: ["IAudioEndpointVolumeCallback","IAudioEndpointVolumeCallback interface [Core Audio]","IAudioEndpointVolumeCallback interface [Core Audio]","described","coreaudio.iaudioendpointvolumecallback","endpointvolume/IAudioEndpointVolumeCallback"]
old-location: coreaudio\iaudioendpointvolumecallback.htm
tech.root: CoreAudio
ms.assetid: 0b631d1b-f89c-4789-a09c-875b24a48a89
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolumeCallback, IAudioEndpointVolumeCallback interface [Core Audio], IAudioEndpointVolumeCallback interface [Core Audio],described, coreaudio.iaudioendpointvolumecallback, endpointvolume/IAudioEndpointVolumeCallback
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioEndpointVolumeCallback
 - endpointvolume/IAudioEndpointVolumeCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolumeCallback
---

# IAudioEndpointVolumeCallback interface


## -description

The <b>IAudioEndpointVolumeCallback</b> interface provides notifications of changes in the volume level and muting state of an audio endpoint device. Unlike the other interfaces in this section, which are implemented by the WASAPI system component, an EndpointVolume API client implements the <b>IAudioEndpointVolumeCallback</b> interface. To receive event notifications, the client passes a pointer to its <b>IAudioEndpointVolumeCallback</b> interface to the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">IAudioEndpointVolume::RegisterControlChangeNotify</a> method.

After registering its <b>IAudioEndpointVolumeCallback</b> interface, the client receives event notifications in the form of callbacks through the <b>OnNotify</b> method in the interface. These event notifications occur when one of the following methods causes a change in the volume level or muting state of an endpoint device:

<ul>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel">IAudioEndpointVolume::SetChannelVolumeLevel</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel">IAudioEndpointVolume::SetMasterVolumeLevel</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar">IAudioEndpointVolume::SetMasterVolumeLevelScalar</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute">IAudioEndpointVolume::SetMute</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown">IAudioEndpointVolume::VolumeStepDown</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup">IAudioEndpointVolume::VolumeStepUp</a>
</li>
</ul>
If an audio endpoint device implements hardware volume and mute controls, the <b>IAudioEndpointVolume</b> interface uses the hardware controls to manage the device's volume. Otherwise, the <b>IAudioEndpointVolume</b> interface implements volume and mute controls in software, transparently to the client.

If a device has hardware volume and mute controls, changes made to the volume and mute settings through the methods in the preceding list affect the device's volume in both shared mode and exclusive mode. If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through these methods affect the device's volume in shared mode, but not in exclusive mode. In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls. However, changes made to the software controls through these methods generate event notifications regardless of whether the device is operating in shared mode or in exclusive mode. Changes made to the software volume and mute controls while the device operates in exclusive mode take effect when the device switches to shared mode.

To determine whether a device has hardware volume and mute controls, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport">IAudioEndpointVolume::QueryHardwareSupport</a> method.

In implementing the <b>IAudioEndpointVolumeCallback</b> interface, the client should observe these rules to avoid deadlocks:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">IAudioEndpointVolume::UnregisterControlChangeNotify</a> method during an event callback.</li>
<li>The client should never release the final reference on an EndpointVolume API object during an event callback.</li>
</ul>
For a code example that implements the <b>IAudioEndpointVolumeCallback</b> interface, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -inheritance

The <b>IAudioEndpointVolumeCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointVolumeCallback</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">IAudioEndpointVolume::RegisterControlChangeNotify</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">IAudioEndpointVolume::UnregisterControlChangeNotify</a>
