---
UID: NF:mmeapi.mixerGetID
title: mixerGetID function (mmeapi.h)
description: The mixerGetID function retrieves the device identifier for a mixer device associated with a specified device handle.
helpviewer_keywords: ["_win32_mixerGetID","mixerGetID","mixerGetID function [Windows Multimedia]","mmeapi/mixerGetID","multimedia.mixergetid"]
old-location: multimedia\mixergetid.htm
tech.root: Multimedia
ms.assetid: e70d6be0-858c-4042-bfaf-6a62bafa269c
ms.date: 12/05/2018
ms.keywords: _win32_mixerGetID, mixerGetID, mixerGetID function [Windows Multimedia], mmeapi/mixerGetID, multimedia.mixergetid
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
 - mixerGetID
 - mmeapi/mixerGetID
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
 - mixerGetID
---

# mixerGetID function


## -description

The <b>mixerGetID</b> function retrieves the device identifier for a mixer device associated with a specified device handle.

## -parameters

### -param hmxobj

Handle to the audio mixer object to map to a mixer device identifier.

### -param puMxId

Pointer to a variable that receives the mixer device identifier. If no mixer device is available for the <i>hmxobj</i> object, the value -1 is placed in this location and the MMSYSERR_NODRIVER error value is returned.

### -param fdwId

Flags for mapping the mixer object <i>hmxobj</i>. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MIXER_OBJECTF_AUX</td>
<td>The <i>hmxobj</i> parameter is an auxiliary device identifier in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd756713(v=vs.85)">auxGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIDIIN</td>
<td>The <i>hmxobj</i> parameter is the handle of a MIDI input device. This handle must have been returned by the <a href="/previous-versions/dd798458(v=vs.85)">midiInOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIDIOUT</td>
<td>The <i>hmxobj</i> parameter is the handle of a MIDI output device. This handle must have been returned by the <a href="/previous-versions/dd798476(v=vs.85)">midiOutOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIXER</td>
<td>The <i>hmxobj</i> parameter is a mixer device handle returned by the <a href="/previous-versions/dd757308(v=vs.85)">mixerOpen</a> function. This flag is optional.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HWAVEIN</td>
<td>The <i>hmxobj</i> parameter is a waveform-audio input handle returned by the <a href="/previous-versions/dd743847(v=vs.85)">waveInOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HWAVEOUT</td>
<td>The <i>hmxobj</i> parameter is a waveform-audio output handle returned by the <a href="/previous-versions/dd743866(v=vs.85)">waveOutOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_MIDIIN</td>
<td>The <i>hmxobj</i> parameter is the identifier of a MIDI input device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd798456(v=vs.85)">midiInGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_MIDIOUT</td>
<td>The <i>hmxobj</i> parameter is the identifier of a MIDI output device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd798472(v=vs.85)">midiOutGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_MIXER</td>
<td>The <i>hmxobj</i> parameter is the identifier of a mixer device in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd757304(v=vs.85)">mixerGetNumDevs</a> function. This flag is optional.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_WAVEIN</td>
<td>The <i>hmxobj</i> parameter is the identifier of a waveform-audio input device in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd743844(v=vs.85)">waveInGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_WAVEOUT</td>
<td>The <i>hmxobj</i> parameter is the identifier of a waveform-audio output device in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd743860(v=vs.85)">waveOutGetNumDevs</a> function.</td>
</tr>
</table>

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hmxobj</i> parameter specifies an invalid device identifier.

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
The <i>hmxobj</i> parameter specifies an invalid handle.

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
No audio mixer device is available for the object specified by <i>hmxobj</i>. The location referenced by <i>puMxId</i> also contains the value -1.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>