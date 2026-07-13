---
UID: NF:mmeapi.mixerGetLineControlsW
title: mixerGetLineControlsW function (mmeapi.h)
description: The mixerGetLineControlsW (Unicode) function retrieves one or more controls associated with an audio line. (mixerGetLineControlsW)
helpviewer_keywords: ["_win32_mixerGetLineControls", "mixerGetLineControls", "mixerGetLineControls function [Windows Multimedia]", "mixerGetLineControlsW", "mmeapi/mixerGetLineControls", "mmeapi/mixerGetLineControlsW", "multimedia.mixergetlinecontrols"]
old-location: multimedia\mixergetlinecontrols.htm
tech.root: Multimedia
ms.assetid: 48fa3396-f3ec-411a-9ea7-d7e82d606f14
ms.date: 08/02/2022
ms.keywords: _win32_mixerGetLineControls, mixerGetLineControls, mixerGetLineControls function [Windows Multimedia], mixerGetLineControlsA, mixerGetLineControlsW, mmeapi/mixerGetLineControls, mmeapi/mixerGetLineControlsA, mmeapi/mixerGetLineControlsW, multimedia.mixergetlinecontrols
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: mixerGetLineControlsW (Unicode) and mixerGetLineControlsA (ANSI)
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
 - mixerGetLineControlsW
 - mmeapi/mixerGetLineControlsW
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
 - mixerGetLineControls
 - mixerGetLineControlsA
 - mixerGetLineControlsW
---

# mixerGetLineControlsW function


## -description

The <b>mixerGetLineControls</b> function retrieves one or more controls associated with an audio line.

## -parameters

### -param hmxobj

Handle to the mixer device object that is being queried.

### -param pmxlc

Pointer to a <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinecontrolsa">MIXERLINECONTROLS</a> structure. This structure is used to reference one or more <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structures to be filled with information about the controls associated with an audio line. The <b>cbStruct</b> member of the <b>MIXERLINECONTROLS</b> structure must always be initialized to be the size, in bytes, of the <b>MIXERLINECONTROLS</b> structure.

### -param fdwControls

Flags for retrieving information about one or more controls associated with an audio line. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>MIXER_GETLINECONTROLSF_ALL</td>
<td>The <i>pmxlc</i> parameter references a list of <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structures that will receive information on all controls associated with the audio line identified by the <b>dwLineID</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinecontrolsa">MIXERLINECONTROLS</a> structure. The <b>cControls</b> member must be initialized to the number of controls associated with the line. This number is retrieved from the <b>cControls</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinea">MIXERLINE</a> structure returned by the <a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a> function. The <b>cbmxctrl</b> member must be initialized to the size, in bytes, of a single <b>MIXERCONTROL</b> structure. The <b>pamxctrl</b> member must point to the first <b>MIXERCONTROL</b> structure to be filled. The <b>dwControlID</b> and <b>dwControlType</b> members are ignored for this query.</td>
</tr>
<tr>
<td>MIXER_GETLINECONTROLSF_ONEBYID</td>
<td>The <i>pmxlc</i> parameter references a single <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structure that will receive information on the control identified by the <b>dwControlID</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinecontrolsa">MIXERLINECONTROLS</a> structure. The <b>cControls</b> member must be initialized to 1. The <b>cbmxctrl</b> member must be initialized to the size, in bytes, of a single <b>MIXERCONTROL</b> structure. The <b>pamxctrl</b> member must point to a <b>MIXERCONTROL</b> structure to be filled. The <b>dwLineID</b> and <b>dwControlType</b> members are ignored for this query. This query is usually used to refresh a control after receiving a <a href="/windows/desktop/Multimedia/mm-mixm-control-change">MM_MIXM_CONTROL_CHANGE</a> control change notification message by the user-defined callback (see <a href="/previous-versions/dd757308(v=vs.85)">mixerOpen</a>).</td>
</tr>
<tr>
<td>MIXER_GETLINECONTROLSF_ONEBYTYPE</td>
<td>The <b>mixerGetLineControls</b> function retrieves information about the first control of a specific class for the audio line that is being queried. The <i>pmxlc</i> parameter references a single <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercontrola">MIXERCONTROL</a> structure that will receive information about the specific control. The audio line is identified by the <b>dwLineID</b> member. The control class is specified in the <b>dwControlType</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinecontrolsa">MIXERLINECONTROLS</a> structure.The <b>dwControlID</b> member is ignored for this query. This query can be used by an application to get information on a single control associated with a line. For example, you might want your application to use a peak meter only from a waveform-audio output line.

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
> The mmeapi.h header defines mixerGetLineControls as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
