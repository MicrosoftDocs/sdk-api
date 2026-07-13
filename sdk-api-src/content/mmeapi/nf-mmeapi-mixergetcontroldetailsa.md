---
UID: NF:mmeapi.mixerGetControlDetailsA
title: mixerGetControlDetailsA function (mmeapi.h)
description: The mixerGetControlDetails function retrieves details about a single control associated with an audio line. (mixerGetControlDetailsA)
helpviewer_keywords: ["mixerGetControlDetailsA"]
old-location: multimedia\mixergetcontroldetails.htm
tech.root: Multimedia
ms.assetid: b1fdd9e7-42cf-41fb-99f7-b7da990e5881
ms.date: 12/05/2018
ms.keywords: _win32_mixerGetControlDetails, mixerGetControlDetails, mixerGetControlDetails function [Windows Multimedia], mixerGetControlDetailsA, mixerGetControlDetailsW, mmsystem/mixerGetControlDetails, mmsystem/mixerGetControlDetailsA, mmsystem/mixerGetControlDetailsW, multimedia.mixergetcontroldetails
req.header: mmeapi.h
req.include-header: Mmeapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mixerGetControlDetailsW (Unicode) and mixerGetControlDetailsA (ANSI)
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
 - mixerGetControlDetailsA
 - mmeapi/mixerGetControlDetailsA
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
 - mixerGetControlDetails
 - mixerGetControlDetailsA
 - mixerGetControlDetailsW
---

# mixerGetControlDetailsA function


## -description

The <b>mixerGetControlDetails</b> function retrieves details about a single control associated with an audio line.

## -parameters

### -param hmxobj

Handle to the mixer device object being queried.

### -param pmxcd

Pointer to a <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta">MIXERCONTROLDETAILS</a> structure, which is filled with state information about the control.

### -param fdwDetails

Flags for retrieving control details. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MIXER_GETCONTROLDETAILSF_LISTTEXT</td>
<td>The <b>paDetails</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta">MIXERCONTROLDETAILS</a> structure points to one or more <a href="/previous-versions/dd757296(v=vs.85)">MIXERCONTROLDETAILS_LISTTEXT</a> structures to receive text labels for multiple-item controls. An application must get all list text items for a multiple-item control at once. This flag cannot be used with MIXERCONTROL_CONTROLTYPE_CUSTOM controls.</td>
</tr>
<tr>
<td>MIXER_GETCONTROLDETAILSF_VALUE</td>
<td>Current values for a control are retrieved. The <b>paDetails</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta">MIXERCONTROLDETAILS</a> structure points to one or more details structures appropriate for the control class.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_AUX</td>
<td>The <i>hmxobj</i> parameter is an auxiliary device identifier in the range of zero to one less than the number of devices returned by the <a href="/previous-versions/dd756713(v=vs.85)">auxGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIDIIN</td>
<td>The <i>hmxobj</i> parameter is the handle of a MIDI (Musical Instrument Digital Interface) input device. This handle must have been returned by the <a href="/previous-versions/dd798458(v=vs.85)">midiInOpen</a> function.</td>
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
<dt><b>MIXERR_INVALCONTROL</b></dt>
</dl>
</td>
<td width="60%">
The control reference is invalid.

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

## -remarks

All members of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta">MIXERCONTROLDETAILS</a> structure must be initialized before calling this function.





> [!NOTE]
> The mmeapi.h header defines mixerGetControlDetails as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>
