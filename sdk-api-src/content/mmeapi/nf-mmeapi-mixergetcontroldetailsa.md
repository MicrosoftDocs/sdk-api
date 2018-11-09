---
UID: NF:mmeapi.mixerGetControlDetailsA
title: mixerGetControlDetailsA function
author: windows-sdk-content
description: The mixerGetControlDetails function retrieves details about a single control associated with an audio line.
old-location: multimedia\mixergetcontroldetails.htm
tech.root: Multimedia
ms.assetid: b1fdd9e7-42cf-41fb-99f7-b7da990e5881
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_win32_mixerGetControlDetails, mixerGetControlDetails, mixerGetControlDetails function [Windows Multimedia], mixerGetControlDetailsA, mixerGetControlDetailsW, mmsystem/mixerGetControlDetails, mmsystem/mixerGetControlDetailsA, mmsystem/mixerGetControlDetailsW, multimedia.mixergetcontroldetails"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mixerGetControlDetailsA function


## -description



The <b>mixerGetControlDetails</b> function retrieves details about a single control associated with an audio line.




## -parameters




### -param hmxobj

Handle to the mixer device object being queried.


### -param pmxcd

Pointer to a <a href="https://msdn.microsoft.com/171605e0-4bfc-47cf-b667-3e73c172aebd">MIXERCONTROLDETAILS</a> structure, which is filled with state information about the control.


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
<td>The <b>paDetails</b> member of the <a href="https://msdn.microsoft.com/171605e0-4bfc-47cf-b667-3e73c172aebd">MIXERCONTROLDETAILS</a> structure points to one or more <a href="https://msdn.microsoft.com/ffd19f8c-2a8c-4b5e-a20d-cd0a8375dd14">MIXERCONTROLDETAILS_LISTTEXT</a> structures to receive text labels for multiple-item controls. An application must get all list text items for a multiple-item control at once. This flag cannot be used with MIXERCONTROL_CONTROLTYPE_CUSTOM controls.</td>
</tr>
<tr>
<td>MIXER_GETCONTROLDETAILSF_VALUE</td>
<td>Current values for a control are retrieved. The <b>paDetails</b> member of the <a href="https://msdn.microsoft.com/171605e0-4bfc-47cf-b667-3e73c172aebd">MIXERCONTROLDETAILS</a> structure points to one or more details structures appropriate for the control class.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_AUX</td>
<td>The <i>hmxobj</i> parameter is an auxiliary device identifier in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/6e36d549-83ba-4a67-b9d7-047e7d3a5613">auxGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIDIIN</td>
<td>The <i>hmxobj</i> parameter is the handle of a MIDI (Musical Instrument Digital Interface) input device. This handle must have been returned by the <a href="https://msdn.microsoft.com/230deaef-9473-426f-a0eb-14e259600e68">midiInOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIDIOUT</td>
<td>The <i>hmxobj</i> parameter is the handle of a MIDI output device. This handle must have been returned by the <a href="https://msdn.microsoft.com/929cd4d1-6912-4456-a6c7-24a819799e46">midiOutOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIXER</td>
<td>The <i>hmxobj</i> parameter is a mixer device handle returned by the <a href="https://msdn.microsoft.com/7977680b-0967-4b85-9926-fc2725681de9">mixerOpen</a> function. This flag is optional.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HWAVEIN</td>
<td>The <i>hmxobj</i> parameter is a waveform-audio input handle returned by the <a href="https://msdn.microsoft.com/41b5b581-d35c-48ad-adcf-659126c4af50">waveInOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HWAVEOUT</td>
<td>The <i>hmxobj</i> parameter is a waveform-audio output handle returned by the <a href="https://msdn.microsoft.com/ef02221b-df45-4fc3-8d9d-f119fa802d34">waveOutOpen</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_MIDIIN</td>
<td>The <i>hmxobj</i> parameter is the identifier of a MIDI input device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/23303bb2-e053-4a19-a63a-4e017b861af6">midiInGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_MIDIOUT</td>
<td>The <i>hmxobj</i> parameter is the identifier of a MIDI output device. This identifier must be in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/f7abf545-3072-478e-9f6e-28b5fb6ab6e5">midiOutGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_MIXER</td>
<td>The <i>hmxobj</i> parameter is the identifier of a mixer device in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/ae3c3a28-1dc1-4e35-99d6-68e629124a89">mixerGetNumDevs</a> function. This flag is optional.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_WAVEIN</td>
<td>The <i>hmxobj</i> parameter is the identifier of a waveform-audio input device in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/d8cb3c6c-edf7-4035-86da-b13fbdeddf6d">waveInGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_WAVEOUT</td>
<td>The <i>hmxobj</i> parameter is the identifier of a waveform-audio output device in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/d9669c1c-36e2-4575-bf88-41c344d9c593">waveOutGetNumDevs</a> function.</td>
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



All members of the <a href="https://msdn.microsoft.com/171605e0-4bfc-47cf-b667-3e73c172aebd">MIXERCONTROLDETAILS</a> structure must be initialized before calling this function.




## -see-also




<a href="https://msdn.microsoft.com/19f53a98-1a01-4954-a5d7-c428aa2bfa38">Audio Mixer Functions</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>
 

 

