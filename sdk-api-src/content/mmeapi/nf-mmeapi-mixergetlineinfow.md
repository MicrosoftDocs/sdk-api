---
UID: NF:mmeapi.mixerGetLineInfoW
title: mixerGetLineInfoW function (mmeapi.h)
description: The mixerGetLineInfoW (Unicode) function retrieves information about a specific line of a mixer device. (mixerGetLineInfoW)
helpviewer_keywords: ["_win32_mixerGetLineInfo", "mixerGetLineInfo", "mixerGetLineInfo function [Windows Multimedia]", "mixerGetLineInfoW", "mmeapi/mixerGetLineInfo", "mmeapi/mixerGetLineInfoW", "multimedia.mixergetlineinfo"]
old-location: multimedia\mixergetlineinfo.htm
tech.root: Multimedia
ms.assetid: 125f09a6-df7f-4aa0-9180-410025b617e2
ms.date: 08/02/2022
ms.keywords: _win32_mixerGetLineInfo, mixerGetLineInfo, mixerGetLineInfo function [Windows Multimedia], mixerGetLineInfoA, mixerGetLineInfoW, mmeapi/mixerGetLineInfo, mmeapi/mixerGetLineInfoA, mmeapi/mixerGetLineInfoW, multimedia.mixergetlineinfo
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mixerGetLineInfoW (Unicode) and mixerGetLineInfoA (ANSI)
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
 - mixerGetLineInfoW
 - mmeapi/mixerGetLineInfoW
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
 - mixerGetLineInfo
 - mixerGetLineInfoA
 - mixerGetLineInfoW
---

# mixerGetLineInfoW function


## -description

The <b>mixerGetLineInfo</b> function retrieves information about a specific line of a mixer device.

## -parameters

### -param hmxobj

Handle to the mixer device object that controls the specific audio line.

### -param pmxl

Pointer to a <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure. This structure is filled with information about the audio line for the mixer device. The <b>cbStruct</b> member must always be initialized to be the size, in bytes, of the <b>MIXERLINE</b> structure.

### -param fdwInfo

Flags for retrieving information about an audio line. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_COMPONENTTYPE</td>
<td>The <i>pmxl</i> parameter will receive information about the first audio line of the type specified in the <b>dwComponentType</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure. This flag is used to retrieve information about an audio line of a specific component type. Remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_DESTINATION</td>
<td>The <i>pmxl</i> parameter will receive information about the destination audio line specified by the <b>dwDestination</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure. This index ranges from zero to one less than the value in the <b>cDestinations</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a> structure. All remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_LINEID</td>
<td>The <i>pmxl</i> parameter will receive information about the audio line specified by the <b>dwLineID</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure. This is usually used to retrieve updated information about the state of an audio line. All remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_SOURCE</td>
<td>The <i>pmxl</i> parameter will receive information about the source audio line specified by the <b>dwDestination</b> and <b>dwSource</b> members of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure. The index specified by <b>dwDestination</b> ranges from zero to one less than the value in the <b>cDestinations</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a> structure. The index specified by <b>dwSource</b> ranges from zero to one less than the value in the <b>cConnections</b> member of the <b>MIXERLINE</b> structure returned for the audio line stored in the <b>dwDestination</b> member. All remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_TARGETTYPE</td>
<td>The <i>pmxl</i> parameter will receive information about the audio line that is for the <b>dwType</b> member of the <b>Target</b> structure, which is a member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure. This flag is used to retrieve information about an audio line that handles the target type (for example, <b>MIXERLINE_TARGETTYPE_WAVEOUT</b>). The application must initialize the <b>dwType</b>, <b>wMid</b>, <b>wPid</b>, <b>vDriverVersion</b> and <b>szPname</b> members of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure before calling <b>mixerGetLineInfo</b>. All of these values can be retrieved from the device capabilities structures for all media devices. Remaining structure members except <b>cbStruct</b> require no further initialization.


<div class="alert"><b>Note</b>  In the ANSI version of this function (<b>mixerGetLineInfoA</b>), you cannot use the ANSI string returned from <b>mixerGetLineInfo</b> or <a href="/previous-versions/dd743857(v=vs.85)">waveOutGetDevCaps</a> for the value of the <b>psPname</b> string when calling <b>mixerGetLineInfo</b> with the <b>MIXER_GETLINEINFOF_TARGETTYPE</b> flag. The reason is that an internal conversion to and from Unicode is performed, which might  result in loss of data. </div>
<div> </div>


</td>
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
<td>The <i>hmxobj</i> parameter is a mixer device identifier in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd757304(v=vs.85)">mixerGetNumDevs</a> function. This flag is optional.</td>
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
<dt><b>MIXERR_INVALLINE</b></dt>
</dl>
</td>
<td width="60%">
The audio line reference is invalid.

</td>
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
No mixer device is available for the object specified by <i>hmxobj</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines mixerGetLineInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
