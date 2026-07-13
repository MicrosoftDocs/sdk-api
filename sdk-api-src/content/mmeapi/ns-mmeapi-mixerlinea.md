---
UID: NS:mmeapi.tagMIXERLINEA
title: MIXERLINEA (mmeapi.h)
description: The MIXERLINE structure describes the state and metrics of an audio line. (MIXERLINEA)
helpviewer_keywords: ["*LPMIXERLINEA","*PMIXERLINEA","MIXERLINE","MIXERLINE structure [Windows Multimedia]","MIXERLINEA","MIXERLINE_COMPONENTTYPE_DST_DIGITAL","MIXERLINE_COMPONENTTYPE_DST_HEADPHONES","MIXERLINE_COMPONENTTYPE_DST_LINE","MIXERLINE_COMPONENTTYPE_DST_MONITOR","MIXERLINE_COMPONENTTYPE_DST_SPEAKERS","MIXERLINE_COMPONENTTYPE_DST_TELEPHONE","MIXERLINE_COMPONENTTYPE_DST_UNDEFINED","MIXERLINE_COMPONENTTYPE_DST_VOICEIN","MIXERLINE_COMPONENTTYPE_DST_WAVEIN","MIXERLINE_COMPONENTTYPE_SRC_ANALOG","MIXERLINE_COMPONENTTYPE_SRC_AUXILIARY","MIXERLINE_COMPONENTTYPE_SRC_COMPACTDISC","MIXERLINE_COMPONENTTYPE_SRC_DIGITAL","MIXERLINE_COMPONENTTYPE_SRC_LINE","MIXERLINE_COMPONENTTYPE_SRC_MICROPHONE","MIXERLINE_COMPONENTTYPE_SRC_PCSPEAKER","MIXERLINE_COMPONENTTYPE_SRC_SYNTHESIZER","MIXERLINE_COMPONENTTYPE_SRC_TELEPHONE","MIXERLINE_COMPONENTTYPE_SRC_UNDEFINED","MIXERLINE_COMPONENTTYPE_SRC_WAVEOUT","MIXERLINE_LINEF_ACTIVE","MIXERLINE_LINEF_DISCONNECTED","MIXERLINE_LINEF_SOURCE","MIXERLINE_TARGETTYPE_AUX","MIXERLINE_TARGETTYPE_MIDIIN","MIXERLINE_TARGETTYPE_MIDIOUT","MIXERLINE_TARGETTYPE_UNDEFINED","MIXERLINE_TARGETTYPE_WAVEIN","MIXERLINE_TARGETTYPE_WAVEOUT","_win32_MIXERLINE_str","mmeapi/MIXERLINE","multimedia.mixerline","tagMIXERLINE","tagMIXERLINEA","tagMIXERLINEW"]
old-location: multimedia\mixerline.htm
tech.root: Multimedia
ms.assetid: a314cdcd-dd52-49f1-92b4-c8e3775dcbe2
ms.date: 12/05/2018
ms.keywords: '*LPMIXERLINEA, *PMIXERLINEA, MIXERLINE, MIXERLINE structure [Windows Multimedia], MIXERLINEA, MIXERLINE_COMPONENTTYPE_DST_DIGITAL, MIXERLINE_COMPONENTTYPE_DST_HEADPHONES, MIXERLINE_COMPONENTTYPE_DST_LINE, MIXERLINE_COMPONENTTYPE_DST_MONITOR, MIXERLINE_COMPONENTTYPE_DST_SPEAKERS, MIXERLINE_COMPONENTTYPE_DST_TELEPHONE, MIXERLINE_COMPONENTTYPE_DST_UNDEFINED, MIXERLINE_COMPONENTTYPE_DST_VOICEIN, MIXERLINE_COMPONENTTYPE_DST_WAVEIN, MIXERLINE_COMPONENTTYPE_SRC_ANALOG, MIXERLINE_COMPONENTTYPE_SRC_AUXILIARY, MIXERLINE_COMPONENTTYPE_SRC_COMPACTDISC, MIXERLINE_COMPONENTTYPE_SRC_DIGITAL, MIXERLINE_COMPONENTTYPE_SRC_LINE, MIXERLINE_COMPONENTTYPE_SRC_MICROPHONE, MIXERLINE_COMPONENTTYPE_SRC_PCSPEAKER, MIXERLINE_COMPONENTTYPE_SRC_SYNTHESIZER, MIXERLINE_COMPONENTTYPE_SRC_TELEPHONE, MIXERLINE_COMPONENTTYPE_SRC_UNDEFINED, MIXERLINE_COMPONENTTYPE_SRC_WAVEOUT, MIXERLINE_LINEF_ACTIVE, MIXERLINE_LINEF_DISCONNECTED, MIXERLINE_LINEF_SOURCE, MIXERLINE_TARGETTYPE_AUX, MIXERLINE_TARGETTYPE_MIDIIN, MIXERLINE_TARGETTYPE_MIDIOUT, MIXERLINE_TARGETTYPE_UNDEFINED, MIXERLINE_TARGETTYPE_WAVEIN, MIXERLINE_TARGETTYPE_WAVEOUT, _win32_MIXERLINE_str, mmeapi/MIXERLINE, multimedia.mixerline, tagMIXERLINE, tagMIXERLINEA, tagMIXERLINEW'
req.header: mmeapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIXERLINEA, *PMIXERLINEA, *LPMIXERLINEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIXERLINEA
 - mmeapi/tagMIXERLINEA
 - PMIXERLINEA
 - mmeapi/PMIXERLINEA
 - MIXERLINEA
 - mmeapi/MIXERLINEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - MIXERLINE
 - MIXERLINEA
---

# MIXERLINEA structure


## -description

The <b>MIXERLINE</b> structure describes the state and metrics of an audio line.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>MIXERLINE</b> structure. This member must be initialized before calling the <a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a> function. The size specified in this member must be large enough to contain the <b>MIXERLINE</b> structure. When <b>mixerGetLineInfo</b> returns, this member contains the actual size of the information returned. The returned information will not exceed the requested size.

### -field dwDestination

Destination line index. This member ranges from zero to one less than the value specified in the <b>cDestinations</b> member of the <a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a> structure retrieved by the <a href="/previous-versions/dd757300(v=vs.85)">mixerGetDevCaps</a> function. When the <a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a> function is called with the MIXER_GETLINEINFOF_DESTINATION flag, properties for the destination line are returned. (The <b>dwSource</b> member must be set to zero in this case.) When called with the MIXER_GETLINEINFOF_SOURCE flag, the properties for the source given by the <b>dwSource</b> member that is associated with the <b>dwDestination</b> member are returned.

### -field dwSource

Index for the audio source line associated with the <b>dwDestination</b> member. That is, this member specifies the <i>n</i>th audio source line associated with the specified audio destination line. This member is not used for destination lines and must be set to zero when MIXER_GETLINEINFOF_DESTINATION is specified in the <a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a> function. When the MIXER_GETLINEINFOF_SOURCE flag is specified, this member ranges from zero to one less than the value specified in the <b>cConnections</b> member for the audio destination line given in the <b>dwDestination</b> member.

### -field dwLineID

An identifier defined by the mixer device that uniquely refers to the audio line described by the <b>MIXERLINE</b> structure. This identifier is unique for each mixer device and can be in any format. An application should use this identifier only as an abstract handle.

### -field fdwLine

Status and support flags for the audio line. This member is always returned to the application and requires no initialization.

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_LINEF_ACTIVE"></a><a id="mixerline_linef_active"></a><dl>
<dt><b>MIXERLINE_LINEF_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is active. An active line indicates that a signal is probably passing through the line.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_LINEF_DISCONNECTED"></a><a id="mixerline_linef_disconnected"></a><dl>
<dt><b>MIXERLINE_LINEF_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Audio line is disconnected. A disconnected line's associated controls can still be modified, but the changes have no effect until the line is connected.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_LINEF_SOURCE"></a><a id="mixerline_linef_source"></a><dl>
<dt><b>MIXERLINE_LINEF_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is an audio source line associated with a single audio destination line. If this flag is not set, this line is an audio destination line associated with zero or more audio source lines.

</td>
</tr>
</table>
 

If an application is not using a waveform-audio output device, the audio line associated with that device would not be active (that is, the MIXERLINE_LINEF_ACTIVE flag would not be set).

If the waveform-audio output device is opened, then the audio line is considered active and the MIXERLINE_LINEF_ACTIVE flag will be set. 

A paused or starved waveform-audio output device is still considered active. In other words, if the waveform-audio output device is opened by an application regardless of whether data is being played, the associated audio line is considered active. 

If a line cannot be strictly defined as active, the mixer device will always set the MIXERLINE_LINEF_ACTIVE flag.

### -field dwUser

Instance data defined by the audio device for the line. This member is intended for custom mixer applications designed specifically for the mixer device returning this information. Other applications should ignore this data.

### -field dwComponentType

Component type for this audio line. An application can use this information to display tailored graphics or to search for a particular component. If an application does not use component types, this member should be ignored. This member can be one of the following values:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_DIGITAL"></a><a id="mixerline_componenttype_dst_digital"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_DIGITAL</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a digital destination (for example, digital input to a DAT or CD audio device).
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_HEADPHONES"></a><a id="mixerline_componenttype_dst_headphones"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_HEADPHONES</b></dt>
</dl>
</td>
<td width="60%">
Audio line is an adjustable (gain and/or attenuation) destination intended to drive headphones. Most audio cards use the same audio destination line for speakers and headphones, in which case the mixer device simply uses the MIXERLINE_COMPONENTTYPE_DST_SPEAKERS type.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_LINE"></a><a id="mixerline_componenttype_dst_line"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_LINE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a line level destination (for example, line level input from a CD audio device) that will be the final recording source for the analog-to-digital converter (ADC). Because most audio cards for personal computers provide some sort of gain for the recording audio source line, the mixer device will use the MIXERLINE_COMPONENTTYPE_DST_WAVEIN type.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_MONITOR"></a><a id="mixerline_componenttype_dst_monitor"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_MONITOR</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a destination used for a monitor.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_SPEAKERS"></a><a id="mixerline_componenttype_dst_speakers"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_SPEAKERS</b></dt>
</dl>
</td>
<td width="60%">
Audio line is an adjustable (gain and/or attenuation) destination intended to drive speakers. This is the typical component type for the audio output of audio cards for personal computers.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_TELEPHONE"></a><a id="mixerline_componenttype_dst_telephone"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_TELEPHONE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a destination that will be routed to a telephone line.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_UNDEFINED"></a><a id="mixerline_componenttype_dst_undefined"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a destination that cannot be defined by one of the standard component types. A mixer device is required to use this component type for line component types that have not been defined by Microsoft Corporation.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_VOICEIN"></a><a id="mixerline_componenttype_dst_voicein"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_VOICEIN</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a destination that will be the final recording source for voice input. This component type is exactly like MIXERLINE_COMPONENTTYPE_DST_WAVEIN but is intended specifically for settings used during voice recording/recognition. Support for this line is optional for a mixer device. Many mixer devices provide only MIXERLINE_COMPONENTTYPE_DST_WAVEIN.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_DST_WAVEIN"></a><a id="mixerline_componenttype_dst_wavein"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_DST_WAVEIN</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a destination that will be the final recording source for the waveform-audio input (ADC). This line typically provides some sort of gain or attenuation. This is the typical component type for the recording line of most audio cards for personal computers.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_ANALOG"></a><a id="mixerline_componenttype_src_analog"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_ANALOG</b></dt>
</dl>
</td>
<td width="60%">
Audio line is an analog source (for example, analog output from a video-cassette tape).
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_AUXILIARY"></a><a id="mixerline_componenttype_src_auxiliary"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_AUXILIARY</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source originating from the auxiliary audio line. This line type is intended as a source with gain or attenuation that can be routed to the MIXERLINE_COMPONENTTYPE_DST_SPEAKERS destination and/or recorded from the MIXERLINE_COMPONENTTYPE_DST_WAVEIN destination.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_COMPACTDISC"></a><a id="mixerline_componenttype_src_compactdisc"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_COMPACTDISC</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source originating from the output of an internal audio CD. This component type is provided for audio cards that provide an audio source line intended to be connected to an audio CD (or CD-ROM playing an audio CD).
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_DIGITAL"></a><a id="mixerline_componenttype_src_digital"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_DIGITAL</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a digital source (for example, digital output from a DAT or audio CD).
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_LINE"></a><a id="mixerline_componenttype_src_line"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_LINE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a line-level source (for example, line-level input from an external stereo) that can be used as an optional recording source. Because most audio cards for personal computers provide some sort of gain for the recording source line, the mixer device will use the MIXERLINE_COMPONENTTYPE_SRC_AUXILIARY type.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_MICROPHONE"></a><a id="mixerline_componenttype_src_microphone"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_MICROPHONE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a microphone recording source. Most audio cards for personal computers provide at least two types of recording sources: an auxiliary audio line and microphone input. A microphone audio line typically provides some sort of gain. Audio cards that use a single input for use with a microphone or auxiliary audio line should use the MIXERLINE_COMPONENTTYPE_SRC_MICROPHONE component type.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_PCSPEAKER"></a><a id="mixerline_componenttype_src_pcspeaker"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_PCSPEAKER</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source originating from personal computer speaker. Several audio cards for personal computers provide the ability to mix what would typically be played on the internal speaker with the output of an audio card. Some audio cards support the ability to use this output as a recording source.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_SYNTHESIZER"></a><a id="mixerline_componenttype_src_synthesizer"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_SYNTHESIZER</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source originating from the output of an internal synthesizer. Most audio cards for personal computers provide some sort of MIDI synthesizer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_TELEPHONE"></a><a id="mixerline_componenttype_src_telephone"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_TELEPHONE</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source originating from an incoming telephone line.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_UNDEFINED"></a><a id="mixerline_componenttype_src_undefined"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source that cannot be defined by one of the standard component types. A mixer device is required to use this component type for line component types that have not been defined by Microsoft Corporation.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_COMPONENTTYPE_SRC_WAVEOUT"></a><a id="mixerline_componenttype_src_waveout"></a><dl>
<dt><b>MIXERLINE_COMPONENTTYPE_SRC_WAVEOUT</b></dt>
</dl>
</td>
<td width="60%">
Audio line is a source originating from the waveform-audio output digital-to-analog converter (DAC). Most audio cards for personal computers provide this component type as a source to the MIXERLINE_COMPONENTTYPE_DST_SPEAKERS destination. Some cards also allow this source to be routed to the MIXERLINE_COMPONENTTYPE_DST_WAVEIN destination.
              

</td>
</tr>
</table>

### -field cChannels

Maximum number of separate channels that can be manipulated independently for the audio line. The minimum value for this field is 1 because a line must have at least one channel. 

Most modern audio cards for personal computers are stereo devices; for them, the value of this member is 2.

Channel 1 is assumed to be the left channel; channel 2 is assumed to be the right channel. 

A multichannel line might have one or more uniform controls (controls that affect all channels of a line uniformly) associated with it.

### -field cConnections

Number of connections that are associated with the audio line. This member is used only for audio destination lines and specifies the number of audio source lines that are associated with it. This member is always zero for source lines and for destination lines that do not have any audio source lines associated with them.

### -field cControls

Number of controls associated with the audio line. This value can be zero. If no controls are associated with the line, the line is likely to be a source that might be selected in a MIXERCONTROL_CONTROLTYPE_MUX or MIXERCONTROL_CONTROLTYPE_MIXER but allows no manipulation of the signal.

### -field szShortName

Short string that describes the audio mixer line specified in the <b>dwLineID</b> member. This description should be appropriate as a concise label for the line.

### -field szName

String that describes the audio mixer line specified in the <b>dwLineID</b> member. This description should be appropriate as a complete description for the line.

### -field Target

Target media information.

### -field Target.dwType

Target media device type associated with the audio line described in the <b>MIXERLINE</b> structure. An application must ignore target information for media device types it does not use. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_TARGETTYPE_AUX"></a><a id="mixerline_targettype_aux"></a><dl>
<dt><b>MIXERLINE_TARGETTYPE_AUX</b></dt>
</dl>
</td>
<td width="60%">
The audio line described by the <b>MIXERLINE</b> structure is strictly bound to the auxiliary device detailed in the remaining members of the <b>Target</b> structure member of the <b>MIXERLINE</b> structure.
                

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_TARGETTYPE_MIDIIN"></a><a id="mixerline_targettype_midiin"></a><dl>
<dt><b>MIXERLINE_TARGETTYPE_MIDIIN</b></dt>
</dl>
</td>
<td width="60%">
The audio line described by the <b>MIXERLINE</b> structure is strictly bound to the MIDI input device detailed in the remaining members of the <b>Target</b> structure member of the <b>MIXERLINE</b> structure.
                

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_TARGETTYPE_MIDIOUT"></a><a id="mixerline_targettype_midiout"></a><dl>
<dt><b>MIXERLINE_TARGETTYPE_MIDIOUT</b></dt>
</dl>
</td>
<td width="60%">
The audio line described by the <b>MIXERLINE</b> structure is strictly bound to the MIDI output device detailed in the remaining members of the <b>Target</b> structure member of the <b>MIXERLINE</b> structure.
                

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_TARGETTYPE_UNDEFINED"></a><a id="mixerline_targettype_undefined"></a><dl>
<dt><b>MIXERLINE_TARGETTYPE_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
The audio line described by the <b>MIXERLINE</b> structure is not strictly bound to a defined media type. All remaining <b>Target</b> structure members of the <b>MIXERLINE</b> structure should be ignored. An application cannot use the MIXERLINE_TARGETTYPE_UNDEFINED target type when calling the <a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a> function with the MIXER_GETLINEINFOF_TARGETTYPE flag.
                

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_TARGETTYPE_WAVEIN"></a><a id="mixerline_targettype_wavein"></a><dl>
<dt><b>MIXERLINE_TARGETTYPE_WAVEIN</b></dt>
</dl>
</td>
<td width="60%">
The audio line described by the <b>MIXERLINE</b> structure is strictly bound to the waveform-audio input device detailed in the remaining members of the <b>Target</b> structure member of the <b>MIXERLINE</b> structure.
                

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERLINE_TARGETTYPE_WAVEOUT"></a><a id="mixerline_targettype_waveout"></a><dl>
<dt><b>MIXERLINE_TARGETTYPE_WAVEOUT</b></dt>
</dl>
</td>
<td width="60%">
The audio line described by the <b>MIXERLINE</b> structure is strictly bound to the waveform-audio output device detailed in the remaining members of the <b>Target</b> structure member of the <b>MIXERLINE</b> structure.
                

</td>
</tr>
</table>

### -field Target.dwDeviceID

Current device identifier of the target media device when the <b>dwType</b> member is a target type other than MIXERLINE_TARGETTYPE_UNDEFINED. This identifier is identical to the current media device index of the associated media device. When calling the <a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a> function with the MIXER_GETLINEINFOF_TARGETTYPE flag, this member is ignored on input and will be returned to the caller by the audio mixer manager.

### -field Target.wMid

Manufacturer identifier of the target media device when the <b>dwType</b> member is a target type other than MIXERLINE_TARGETTYPE_UNDEFINED. This identifier is identical to the <b>wMid</b> member of the device-capabilities structure for the associated media. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field Target.wPid

Product identifier of the target media device when the <b>dwType</b> member is a target type other than MIXERLINE_TARGETTYPE_UNDEFINED. This identifier is identical to the <b>wPid</b> member of the device-capabilities structure for the associated media. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field Target.vDriverVersion

Driver version of the target media device when the <b>dwType</b> member is a target type other than MIXERLINE_TARGETTYPE_UNDEFINED. This version is identical to the <b>vDriverVersion</b> member of the device-capabilities structure for the associated media.

### -field Target.szPname

Product name of the target media device when the <b>dwType</b> member is a target type other than MIXERLINE_TARGETTYPE_UNDEFINED. This name is identical to the <b>szPname</b> member of the device-capabilities structure for the associated media.

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



Audio Mixers



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixercapsa">MIXERCAPS</a>



<a href="/previous-versions/dd757300(v=vs.85)">mixerGetDevCaps</a>



<a href="/previous-versions/dd757303(v=vs.85)">mixerGetLineInfo</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines MIXERLINE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
