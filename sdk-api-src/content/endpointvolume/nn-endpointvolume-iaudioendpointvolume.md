---
UID: NN:endpointvolume.IAudioEndpointVolume
title: IAudioEndpointVolume (endpointvolume.h)
description: The IAudioEndpointVolume interface represents the volume controls on the audio stream to or from an audio endpoint device.
helpviewer_keywords: ["IAudioEndpointVolume","IAudioEndpointVolume interface [Core Audio]","IAudioEndpointVolume interface [Core Audio]","described","coreaudio.iaudioendpointvolume","endpointvolume/IAudioEndpointVolume"]
old-location: coreaudio\iaudioendpointvolume.htm
tech.root: CoreAudio
ms.assetid: 5e3e7ffc-8822-4b1b-b9af-206ec1e767e2
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume, IAudioEndpointVolume interface [Core Audio], IAudioEndpointVolume interface [Core Audio],described, coreaudio.iaudioendpointvolume, endpointvolume/IAudioEndpointVolume
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
 - IAudioEndpointVolume
 - endpointvolume/IAudioEndpointVolume
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
 - IAudioEndpointVolume
---

# IAudioEndpointVolume interface


## -description

The <b>IAudioEndpointVolume</b> interface represents the volume controls on the audio stream to or from an audio endpoint device. A client obtains a reference to the <b>IAudioEndpointVolume</b> interface of an endpoint device by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioEndpointVolume.

Audio applications that use the <a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a> and <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> typically use the <a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume</a> interface to manage stream volume levels on a per-session basis. In rare cases, a specialized audio application might require the use of the <b>IAudioEndpointVolume</b> interface to control the master volume level of an audio endpoint device. A client of <b>IAudioEndpointVolume</b> must take care to avoid the potentially disruptive effects on other audio applications of altering the master volume levels of audio endpoint devices. Typically, the user has exclusive control over the master volume levels through the Windows volume-control program, Sndvol.exe.

If the adapter device that streams audio data to or from the endpoint device has hardware volume and mute controls, the <b>IAudioEndpointVolume</b> interface uses those controls to manage the volume and mute settings of the audio stream. If the audio device lacks a hardware volume control for the stream, the audio engine automatically implements volume and mute controls in software.

For applications that manage shared-mode streams to and from endpoint devices, the behavior of the <b>IAudioEndpointVolume</b> is different for rendering streams and capture streams.

For a shared-mode rendering stream, the endpoint volume control that the client accesses through the <b>IAudioEndpointVolume</b> interface operates independently of the per-session volume controls that the <b>ISimpleAudioVolume</b> and <a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interfaces implement. Thus, the volume level of the rendering stream results from the combined effects of the endpoint volume control and per-session controls.

For a shared-mode capture stream, the per-session volume controls that the <b>ISimpleAudioVolume</b> and <b>IChannelAudioVolume</b> interfaces implement are tied directly to the endpoint volume control implemented by the <b>IAudioEndpointVolume</b> interface. Changing the per-session volume control through the methods in the <b>ISimpleAudioVolume</b> and <b>IChannelAudioVolume</b> interfaces changes the setting of the <b>IAudioEndpointVolume</b> interface's volume control, and the reverse is also true. The volume levels represented by each of the interfaces correspond to each other as follows:<ul>
<li> For each channel in a stream, <b>IAudioEndpointVolume</b> provides <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">audio-tapered</a> volume levels expressed in decibels (dB), that are mapped to normalized values in the range from 0.0 (minimum volume) to 1.0 (maximum volume). The possible range is dependent on the audio driver. See <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a> for details.</li>
<li>The session volume represented by <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-getmastervolume">ISimpleAudioVolume::GetMasterVolume</a> is the scalar value ranging from 0.0 to 1.0 that corresponds to the highest volume setting across the various channels.  So, for example, if the left channel is set to 0.8, and the right channel is set to 0.4, then <b>ISimpleAudioVolume::GetMasterVolume</b> will return 0.8.
</li>
<li>When the per-channel volume level is controlled through the methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interface, the scalar indicating volume is always relative to the session volume.  This means that the channel or channels with the highest volume has a volume of 1.0.  Given the example of two channels, set to volumes of  0.8 and 0.4 by <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>, <a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelvolume">IChannelAudioVolume::GetChannelVolume</a> will indicate volumes of 1.0 and 0.5.
</li>
</ul>
<div class="alert"><b>Note</b>  Clients of the <b>EndpointVolume</b> API should not rely on the preceding behavior because it might change in future releases.</div>
<div> </div>


If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the <b>IAudioEndpointVolume</b> interface affect the volume level in both shared mode and exclusive mode. If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the <b>IAudioEndpointVolume</b> interface affect the volume level in shared mode, but not in exclusive mode. In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls. However, the software controls are persistent, and volume changes made while the device operates in exclusive mode take effect when the device switches to shared-mode operation.

To determine whether a device has hardware volume and mute controls, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport">IAudioEndpointVolume::QueryHardwareSupport</a> method.

The methods of the <b>IAudioEndpointVolume</b> interface enable the client to express volume levels either in decibels or as normalized, audio-tapered values. In the latter case, a volume level is expressed as a floating-point value in the normalized range from 0.0 (minimum volume) to 1.0 (maximum volume). Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. For more information about audio-tapered curves, see <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

In addition, to conveniently support volume sliders in user interfaces, the <b>IAudioEndpointVolume</b> interface enables clients to set and get volume levels that are expressed as discrete values or "steps". The steps are uniformly distributed over a nonlinear, audio-tapered curve. If the range contains <i>n</i> steps, the steps are numbered from 0 to <i>n</i>– 1, where step 0 represents the minimum volume level and step <i>n</i>– 1 represents the maximum.

For a code example that uses the <b>IAudioEndpointVolume</b> interface, see <a href="/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.

## -inheritance

The <b>IAudioEndpointVolume</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointVolume</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>
