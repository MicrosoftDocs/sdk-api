---
UID: NF:mmeapi.mixerOpen
title: mixerOpen function (mmeapi.h)
description: The mixerOpen function opens a specified mixer device and ensures that the device will not be removed until the application closes the handle.
helpviewer_keywords: ["_win32_mixerOpen","mixerOpen","mixerOpen function [Windows Multimedia]","mmeapi/mixerOpen","multimedia.mixeropen"]
old-location: multimedia\mixeropen.htm
tech.root: Multimedia
ms.assetid: 7977680b-0967-4b85-9926-fc2725681de9
ms.date: 12/05/2018
ms.keywords: _win32_mixerOpen, mixerOpen, mixerOpen function [Windows Multimedia], mmeapi/mixerOpen, multimedia.mixeropen
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mixerOpen
 - mmeapi/mixerOpen
dev_langs:
 - c++
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
---

# mixerOpen function


## -description

The <b>mixerOpen</b> function opens a specified mixer device and ensures that the device will not be removed until the application closes the handle.

## -parameters

### -param phmx

Pointer to a variable that will receive a handle identifying the opened mixer device. Use this handle to identify the device when calling other audio mixer functions. This parameter cannot be <b>NULL</b>.

### -param uMxId

Identifier of the mixer device to open. Use a valid device identifier or any <b>HMIXEROBJ</b> (see the <a href="/previous-versions/dd757301(v=vs.85)">mixerGetID</a> function for a description of mixer object handles). A "mapper" for audio mixer devices does not currently exist, so a mixer device identifier of -1 is not valid.

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
<td>The <i>uMxId</i> parameter is an auxiliary device identifier in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd756713(v=vs.85)">auxGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HMIDIIN</b></td>
<td>The <i>uMxId</i> parameter is the handle of a MIDI input device. This handle must have been returned by the <a href="/previous-versions/dd798458(v=vs.85)">midiInOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HMIDIOUT</b></td>
<td>The <i>uMxId</i> parameter is the handle of a MIDI output device. This handle must have been returned by the <a href="/previous-versions/dd798476(v=vs.85)">midiOutOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HMIXER</b></td>
<td>The <i>uMxId</i> parameter is a mixer device handle returned by the <b>mixerOpen</b> function. This flag is optional.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HWAVEIN</b></td>
<td>The <i>uMxId</i> parameter is a waveform-audio input handle returned by the <a href="/previous-versions/dd743847(v=vs.85)">waveInOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_HWAVEOUT</b></td>
<td>The <i>uMxId</i> parameter is a waveform-audio output handle returned by the <a href="/previous-versions/dd743866(v=vs.85)">waveOutOpen</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_MIDIIN</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a MIDI input device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd798456(v=vs.85)">midiInGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_MIDIOUT</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a MIDI output device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd798472(v=vs.85)">midiOutGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_MIXER</b></td>
<td>The <i>uMxId</i> parameter is a mixer device identifier in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd757304(v=vs.85)">mixerGetNumDevs</a> function. This flag is optional.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_WAVEIN</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a waveform-audio input device in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd743844(v=vs.85)">waveInGetNumDevs</a> function.</td>
</tr>
<tr>
<td><b>MIXER_OBJECTF_WAVEOUT</b></td>
<td>The <i>uMxId</i> parameter is the identifier of a waveform-audio output device in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd743860(v=vs.85)">waveOutGetNumDevs</a> function.</td>
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

Use the <a href="/previous-versions/dd757304(v=vs.85)">mixerGetNumDevs</a> function to determine the number of audio mixer devices present in the system. The device identifier specified by <i>uMxId</i> varies from zero to one less than the number of devices present.

If a window is chosen to receive callback information, the <a href="/windows/desktop/Multimedia/mm-mixm-line-change">MM_MIXM_LINE_CHANGE</a> and <a href="/windows/desktop/Multimedia/mm-mixm-control-change">MM_MIXM_CONTROL_CHANGE</a> messages are sent to the window procedure function to indicate when an audio line or control state changes. For both messages, the <i>wParam</i> parameter is the handle of the mixer device. The <i>lParam</i> parameter is the line identifier for <b>MM_MIXM_LINE_CHANGE</b> or the control identifier for <b>MM_MIXM_CONTROL_CHANGE</b> that changed state.

To query for audio mixer support or a media device, use the <a href="/previous-versions/dd757301(v=vs.85)">mixerGetID</a> function.

On 64-bit systems, this function may not work as expected in situations where you pass a 64-bit <b>LPHWAVEOUT</b> pointer in the <i>uMxId</i> parameter, because the <i>uMxId</i> parameter is truncated to 32 bits.

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>