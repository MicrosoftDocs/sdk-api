---
UID: NF:mmeapi.mixerGetLineInfo
title: mixerGetLineInfo function (mmeapi.h)
author: windows-sdk-content
description: The mixerGetLineInfo function retrieves information about a specific line of a mixer device.
old-location: multimedia\mixergetlineinfo.htm
tech.root: Multimedia
ms.assetid: 125f09a6-df7f-4aa0-9180-410025b617e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_mixerGetLineInfo, mixerGetLineInfo, mixerGetLineInfo function [Windows Multimedia], mixerGetLineInfoA, mixerGetLineInfoW, mmeapi/mixerGetLineInfo, mmeapi/mixerGetLineInfoA, mmeapi/mixerGetLineInfoW, multimedia.mixergetlineinfo"
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mixerGetLineInfo function


## -description



The <b>mixerGetLineInfo</b> function retrieves information about a specific line of a mixer device.




## -parameters




### -param hmxobj

Handle to the mixer device object that controls the specific audio line.


### -param pmxl

Pointer to a <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure. This structure is filled with information about the audio line for the mixer device. The <b>cbStruct</b> member must always be initialized to be the size, in bytes, of the <b>MIXERLINE</b> structure.


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
<td>The <i>pmxl</i> parameter will receive information about the first audio line of the type specified in the <b>dwComponentType</b> member of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure. This flag is used to retrieve information about an audio line of a specific component type. Remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_DESTINATION</td>
<td>The <i>pmxl</i> parameter will receive information about the destination audio line specified by the <b>dwDestination</b> member of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure. This index ranges from zero to one less than the value in the <b>cDestinations</b> member of the <a href="https://msdn.microsoft.com/4a4220cb-fdb1-4afe-821f-27f5adb51530">MIXERCAPS</a> structure. All remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_LINEID</td>
<td>The <i>pmxl</i> parameter will receive information about the audio line specified by the <b>dwLineID</b> member of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure. This is usually used to retrieve updated information about the state of an audio line. All remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_SOURCE</td>
<td>The <i>pmxl</i> parameter will receive information about the source audio line specified by the <b>dwDestination</b> and <b>dwSource</b> members of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure. The index specified by <b>dwDestination</b> ranges from zero to one less than the value in the <b>cDestinations</b> member of the <a href="https://msdn.microsoft.com/4a4220cb-fdb1-4afe-821f-27f5adb51530">MIXERCAPS</a> structure. The index specified by <b>dwSource</b> ranges from zero to one less than the value in the <b>cConnections</b> member of the <b>MIXERLINE</b> structure returned for the audio line stored in the <b>dwDestination</b> member. All remaining structure members except <b>cbStruct</b> require no further initialization.</td>
</tr>
<tr>
<td>MIXER_GETLINEINFOF_TARGETTYPE</td>
<td>The <i>pmxl</i> parameter will receive information about the audio line that is for the <b>dwType</b> member of the <b>Target</b> structure, which is a member of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure. This flag is used to retrieve information about an audio line that handles the target type (for example, <b>MIXERLINE_TARGETTYPE_WAVEOUT</b>). The application must initialize the <b>dwType</b>, <b>wMid</b>, <b>wPid</b>, <b>vDriverVersion</b> and <b>szPname</b> members of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure before calling <b>mixerGetLineInfo</b>. All of these values can be retrieved from the device capabilities structures for all media devices. Remaining structure members except <b>cbStruct</b> require no further initialization.


<div class="alert"><b>Note</b>  In the ANSI version of this function (<b>mixerGetLineInfoA</b>), you cannot use the ANSI string returned from <b>mixerGetLineInfo</b> or <a href="https://msdn.microsoft.com/294daf81-d52a-44b4-b22a-d75ad6e05fee">waveOutGetDevCaps</a> for the value of the <b>psPname</b> string when calling <b>mixerGetLineInfo</b> with the <b>MIXER_GETLINEINFOF_TARGETTYPE</b> flag. The reason is that an internal conversion to and from Unicode is performed, which might  result in loss of data. </div>
<div> </div>


</td>
</tr>
<tr>
<td>MIXER_OBJECTF_AUX</td>
<td>The <i>hmxobj</i> parameter is an auxiliary device identifier in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/6e36d549-83ba-4a67-b9d7-047e7d3a5613">auxGetNumDevs</a> function.</td>
</tr>
<tr>
<td>MIXER_OBJECTF_HMIDIIN</td>
<td>The <i>hmxobj</i> parameter is the handle of a MIDI input device. This handle must have been returned by the <a href="https://msdn.microsoft.com/230deaef-9473-426f-a0eb-14e259600e68">midiInOpen</a> function.</td>
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
<td>The <i>hmxobj</i> parameter is a mixer device identifier in the range of zero to one less than the number of devices returned by the <a href="https://msdn.microsoft.com/ae3c3a28-1dc1-4e35-99d6-68e629124a89">mixerGetNumDevs</a> function. This flag is optional.</td>
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




<a href="https://msdn.microsoft.com/19f53a98-1a01-4954-a5d7-c428aa2bfa38">Audio Mixer Functions</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>
 

 

