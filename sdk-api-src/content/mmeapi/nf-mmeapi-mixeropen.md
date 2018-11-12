---
UID: NF:mmeapi.mixerOpen
title: mixerOpen function
author: windows-sdk-content
description: The mixerOpen function opens a specified mixer device and ensures that the device will not be removed until the application closes the handle.
old-location: multimedia\mixeropen.htm
tech.root: Multimedia
ms.assetid: 7977680b-0967-4b85-9926-fc2725681de9
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_win32_mixerOpen, mixerOpen, mixerOpen function [Windows Multimedia], mmeapi/mixerOpen, multimedia.mixeropen"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - mixerOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mixerOpen function


## -description



The <b>mixerOpen</b> function opens a specified mixer device and ensures that the device will not be removed until the application closes the handle.




## -parameters




### -param phmx

Pointer to a variable that will receive a handle identifying the opened mixer device. Use this handle to identify the device when calling other audio mixer functions. This parameter cannot be <b>NULL</b>.
          


### -param uMxId

Identifier of the mixer device to open. Use a valid device identifier or any <b>HMIXEROBJ</b> (see the <a href="https://msdn.microsoft.com/e70d6be0-858c-4042-bfaf-6a62bafa269c">mixerGetID</a> function for a description of mixer object handles). A "mapper" for audio mixer devices does not currently exist, so a mixer device identifier of -1 is not valid.
          


### -param dwCallback

Handle to a window called when the state of an audio line and/or control associated with the device being opened is changed. Specify <b>NULL</b> for this parameter if no callback mechanism is to be used.
          


### -param dwInstance

Reserved. Must be zero.


### -param fdwOpen

Flags for opening the device. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td><b>CALLBACK_WINDOW</b></td>
<td>The <i>dwCallback</i> parameter is assumed to be a window handle (<b>HWND</b>).</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_AUX</b></td>
<td>The <i>uMxId</i> parameter is an auxiliary device identifier in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/6e36d549-83ba-4a67-b9d7-047e7d3a5613">auxGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HMIDIIN</b></td>
<td>The <i>uMxId</i> parameter is the handle of a MIDI input device. This handle must have been returned by the <a href="https://msdn.microsoft.com/230deaef-9473-426f-a0eb-14e259600e68">midiInOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HMIDIOUT</b></td>
<td>The <i>uMxId</i> parameter is the handle of a MIDI output device. This handle must have been returned by the <a href="https://msdn.microsoft.com/929cd4d1-6912-4456-a6c7-24a819799e46">midiOutOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HMIXER</b></td>
<td>The <i>uMxId</i> parameter is a mixer device handle returned by the <b>mixerOpen</b> function. This flag is optional.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HWAVEIN</b></td>
<td>The <i>uMxId</i> parameter is a waveform-audio input handle returned by the <a href="https://msdn.microsoft.com/41b5b581-d35c-48ad-adcf-659126c4af50">waveInOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HWAVEOUT</b></td>
<td>The <i>uMxId</i> parameter is a waveform-audio output handle returned by the <a href="https://msdn.microsoft.com/ef02221b-df45-4fc3-8d9d-f119fa802d34">waveOutOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_MIDIIN</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a MIDI input device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/23303bb2-e053-4a19-a63a-4e017b861af6">midiInGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_MIDIOUT</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a MIDI output device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/f7abf545-3072-478e-9f6e-28b5fb6ab6e5">midiOutGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_MIXER</b></td>
<td>The <i>uMxId</i> parameter is a mixer device identifier in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/ae3c3a28-1dc1-4e35-99d6-68e629124a89">mixerGetNumDevs</a> function. This flag is optional.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_WAVEIN</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a waveform-audio input device in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/d8cb3c6c-edf7-4035-86da-b13fbdeddf6d">waveInGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_WAVEOUT</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a waveform-audio output device in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/d9669c1c-36e2-4575-bf88-41c344d9c593">waveOutGetNumDevs</a> function.</td>
</tr>
</table>
 


## -returns



Returns <b>MMSYSERR_NOERROR</b> if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ALLOCATED</b></dt>
</dl>
</td>
<td width="60%">
The specified resource is already allocated by the maximum number of clients possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
The <i>uMxId</i> parameter specifies an invalid device identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
One or more flags are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>uMxId</i> parameter specifies an invalid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No mixer device is available for the object specified by <i>uMxId</i>. Note that the location referenced by <i>uMxId</i> will also contain the value –1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate resources.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/ae3c3a28-1dc1-4e35-99d6-68e629124a89">mixerGetNumDevs</a> function to determine the number of audio mixer devices present in the system. The device identifier specified by <i>uMxId</i> varies from zero to one less than the number of devices present.

If a window is chosen to receive callback information, the <a href="https://msdn.microsoft.com/68ada0be-9dc5-4edf-b924-ef0d10a1b79a">MM_MIXM_LINE_CHANGE</a> and <a href="https://msdn.microsoft.com/921c55a7-86c0-43d1-b817-bfbd3c4bb28b">MM_MIXM_CONTROL_CHANGE</a> messages are sent to the window procedure function to indicate when an audio line or control state changes. For both messages, the <i>wParam</i> parameter is the handle of the mixer device. The <i>lParam</i> parameter is the line identifier for <b>MM_MIXM_LINE_CHANGE</b> or the control identifier for <b>MM_MIXM_CONTROL_CHANGE</b> that changed state.

To query for audio mixer support or a media device, use the <a href="https://msdn.microsoft.com/e70d6be0-858c-4042-bfaf-6a62bafa269c">mixerGetID</a> function.

On 64-bit systems, this function may not work as expected in situations where you pass a 64-bit <b>LPHWAVEOUT</b> pointer in the <i>uMxId</i> parameter, because the <i>uMxId</i> parameter is truncated to 32 bits.  




## -see-also




<a href="https://msdn.microsoft.com/19f53a98-1a01-4954-a5d7-c428aa2bfa38">Audio Mixer Functions</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>
 

 

