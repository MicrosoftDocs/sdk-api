---
UID: NN:endpointvolume.IAudioEndpointVolume
title: IAudioEndpointVolume (endpointvolume.h)
author: windows-sdk-content
description: The IAudioEndpointVolume interface represents the volume controls on the audio stream to or from an audio endpoint device.
old-location: coreaudio\iaudioendpointvolume.htm
tech.root: CoreAudio
ms.assetid: 5e3e7ffc-8822-4b1b-b9af-206ec1e767e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume, IAudioEndpointVolume interface [Core Audio], IAudioEndpointVolume interface [Core Audio],described, coreaudio.iaudioendpointvolume, endpointvolume/IAudioEndpointVolume
ms.topic: interface
f1_keywords: 
 - "endpointvolume/IAudioEndpointVolume"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointVolume interface


## -description



The <b>IAudioEndpointVolume</b> interface represents the volume controls on the audio stream to or from an audio endpoint device. A client obtains a reference to the <b>IAudioEndpointVolume</b> interface of an endpoint device by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to REFIID IID_IAudioEndpointVolume.

Audio applications that use the <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a> and <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a> typically use the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume</a> interface to manage stream volume levels on a per-session basis. In rare cases, a specialized audio application might require the use of the <b>IAudioEndpointVolume</b> interface to control the master volume level of an audio endpoint device. A client of <b>IAudioEndpointVolume</b> must take care to avoid the potentially disruptive effects on other audio applications of altering the master volume levels of audio endpoint devices. Typically, the user has exclusive control over the master volume levels through the Windows volume-control program, Sndvol.exe.

If the adapter device that streams audio data to or from the endpoint device has hardware volume and mute controls, the <b>IAudioEndpointVolume</b> interface uses those controls to manage the volume and mute settings of the audio stream. If the audio device lacks a hardware volume control for the stream, the audio engine automatically implements volume and mute controls in software.

For applications that manage shared-mode streams to and from endpoint devices, the behavior of the <b>IAudioEndpointVolume</b> is different for rendering streams and capture streams.

For a shared-mode rendering stream, the endpoint volume control that the client accesses through the <b>IAudioEndpointVolume</b> interface operates independently of the per-session volume controls that the <b>ISimpleAudioVolume</b> and <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interfaces implement. Thus, the volume level of the rendering stream results from the combined effects of the endpoint volume control and per-session controls.

For a shared-mode capture stream, the per-session volume controls that the <b>ISimpleAudioVolume</b> and <b>IChannelAudioVolume</b> interfaces implement are tied directly to the endpoint volume control implemented by the <b>IAudioEndpointVolume</b> interface. Changing the per-session volume control through the methods in the <b>ISimpleAudioVolume</b> and <b>IChannelAudioVolume</b> interfaces changes the setting of the <b>IAudioEndpointVolume</b> interface's volume control, and the reverse is also true. The volume levels represented by each of the interfaces correspond to each other as follows:<ul>
<li> For each channel in a stream, <b>IAudioEndpointVolume</b> provides <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-tapered-volume-controls">audio-tapered</a> volume levels expressed in decibels (dB), that are mapped to normalized values in the range from 0.0 (minimum volume) to 1.0 (maximum volume). The possible range is dependent on the audio driver. See <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a> for details.</li>
<li>The session volume represented by <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-getmastervolume">ISimpleAudioVolume::GetMasterVolume</a> is the scalar value ranging from 0.0 to 1.0 that corresponds to the highest volume setting across the various channels.  So, for example, if the left channel is set to 0.8, and the right channel is set to 0.4, then <b>ISimpleAudioVolume::GetMasterVolume</b> will return 0.8.
</li>
<li>When the per-channel volume level is controlled through the methods in the <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interface, the scalar indicating volume is always relative to the session volume.  This means that the channel or channels with the highest volume has a volume of 1.0.  Given the example of two channels, set to volumes of  0.8 and 0.4 by <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>, <a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelvolume">IChannelAudioVolume::GetChannelVolume</a> will indicate volumes of 1.0 and 0.5.
</li>
</ul>
<div class="alert"><b>Note</b>  Clients of the <b>EndpointVolume</b> API should not rely on the preceding behavior because it might change in future releases.</div>
<div> </div>


If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the <b>IAudioEndpointVolume</b> interface affect the volume level in both shared mode and exclusive mode. If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the <b>IAudioEndpointVolume</b> interface affect the volume level in shared mode, but not in exclusive mode. In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls. However, the software controls are persistent, and volume changes made while the device operates in exclusive mode take effect when the device switches to shared-mode operation.

To determine whether a device has hardware volume and mute controls, call the <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport">IAudioEndpointVolume::QueryHardwareSupport</a> method.

The methods of the <b>IAudioEndpointVolume</b> interface enable the client to express volume levels either in decibels or as normalized, audio-tapered values. In the latter case, a volume level is expressed as a floating-point value in the normalized range from 0.0 (minimum volume) to 1.0 (maximum volume). Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. For more information about audio-tapered curves, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

In addition, to conveniently support volume sliders in user interfaces, the <b>IAudioEndpointVolume</b> interface enables clients to set and get volume levels that are expressed as discrete values or "steps". The steps are uniformly distributed over a nonlinear, audio-tapered curve. If the range contains <i>n</i> steps, the steps are numbered from 0 to <i>n</i>– 1, where step 0 represents the minimum volume level and step <i>n</i>– 1 represents the maximum.

For a code example that uses the <b>IAudioEndpointVolume</b> interface, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/endpoint-volume-controls">Endpoint Volume Controls</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointVolume</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">GetChannelCount</a>
</td>
<td align="left" width="63%">
Gets a count of the channels in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevel">GetChannelVolumeLevel</a>
</td>
<td align="left" width="63%">
Gets the volume level, in decibels, of the specified channel in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelvolumelevelscalar">GetChannelVolumeLevelScalar</a>
</td>
<td align="left" width="63%">
Gets the normalized, audio-tapered volume level of the specified channel of the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevel">GetMasterVolumeLevel</a>
</td>
<td align="left" width="63%">
Gets the master volume level of the audio stream, in decibels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmastervolumelevelscalar">GetMasterVolumeLevelScalar</a>
</td>
<td align="left" width="63%">
Gets the master volume level, expressed as a normalized, audio-tapered value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getmute">GetMute</a>
</td>
<td align="left" width="63%">
Gets the muting state of the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">GetVolumeRange</a>
</td>
<td align="left" width="63%">
Gets the volume range of the audio stream, in decibels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo">GetVolumeStepInfo</a>
</td>
<td align="left" width="63%">
Gets information about the current step in the volume range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport">QueryHardwareSupport</a>
</td>
<td align="left" width="63%">
Queries the audio endpoint device for its hardware-supported functions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify">RegisterControlChangeNotify</a>
</td>
<td align="left" width="63%">
Registers a client's notification callback interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel">SetChannelVolumeLevel</a>
</td>
<td align="left" width="63%">
Sets the volume level, in decibels, of the specified channel of the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar">SetChannelVolumeLevelScalar</a>
</td>
<td align="left" width="63%">
Sets the normalized, audio-tapered volume level of the specified channel in the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel">SetMasterVolumeLevel</a>
</td>
<td align="left" width="63%">
Sets the master volume level of the audio stream, in decibels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar">SetMasterVolumeLevelScalar</a>
</td>
<td align="left" width="63%">
Sets the master volume level, expressed as a normalized, audio-tapered value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute">SetMute</a>
</td>
<td align="left" width="63%">
Sets the muting state of the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify">UnregisterControlChangeNotify</a>
</td>
<td align="left" width="63%">
Deletes the registration of a client's notification callback interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown">VolumeStepDown</a>
</td>
<td align="left" width="63%">
Decreases the volume level by one step.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup">VolumeStepUp</a>
</td>
<td align="left" width="63%">
Increases the volume level by one step.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>
 

 

