---
UID: NS:mmeapi.tagMIXERCONTROLW
title: MIXERCONTROLW (mmeapi.h)
description: The MIXERCONTROL structure describes the state and metrics of a single control for an audio line. (mixercontrolw)
helpviewer_keywords: ["*LPMIXERCONTROLW","*PMIXERCONTROLW","MIXERCONTROL","MIXERCONTROL structure [Windows Multimedia]","MIXERCONTROL","*PMIXERCONTROL","FAR *PMIXERCONTROL","MIXERCONTROL","*PMIXERCONTROL","FAR *PMIXERCONTROL structure [Windows Multimedia]","MIXERCONTROLW","MIXERCONTROL_CONTROLF_DISABLED","MIXERCONTROL_CONTROLF_MULTIPLE","MIXERCONTROL_CONTROLF_UNIFORM","MIXERCONTROL_CT_CLASS_CUSTOM","MIXERCONTROL_CT_CLASS_FADER","MIXERCONTROL_CT_CLASS_LIST","MIXERCONTROL_CT_CLASS_METER","MIXERCONTROL_CT_CLASS_NUMBER","MIXERCONTROL_CT_CLASS_SLIDER","MIXERCONTROL_CT_CLASS_SWITCH","MIXERCONTROL_CT_CLASS_TIME","_win32_MIXERCONTROL_str","mmeapi/MIXERCONTROL","multimedia.mixercontrol","tMIXERCONTROL","tagMIXERCONTROLA","tagMIXERCONTROLW"]
old-location: multimedia\mixercontrol.htm
tech.root: Multimedia
ms.assetid: 2ddbcf82-9204-43c6-8235-8bce6a55bb36
ms.date: 12/05/2018
ms.keywords: '*LPMIXERCONTROLW, *PMIXERCONTROLW, MIXERCONTROL, MIXERCONTROL structure [Windows Multimedia], MIXERCONTROL,*PMIXERCONTROL,FAR *PMIXERCONTROL, MIXERCONTROL,*PMIXERCONTROL,FAR *PMIXERCONTROL structure [Windows Multimedia], MIXERCONTROLW, MIXERCONTROL_CONTROLF_DISABLED, MIXERCONTROL_CONTROLF_MULTIPLE, MIXERCONTROL_CONTROLF_UNIFORM, MIXERCONTROL_CT_CLASS_CUSTOM, MIXERCONTROL_CT_CLASS_FADER, MIXERCONTROL_CT_CLASS_LIST, MIXERCONTROL_CT_CLASS_METER, MIXERCONTROL_CT_CLASS_NUMBER, MIXERCONTROL_CT_CLASS_SLIDER, MIXERCONTROL_CT_CLASS_SWITCH, MIXERCONTROL_CT_CLASS_TIME, _win32_MIXERCONTROL_str, mmeapi/MIXERCONTROL, multimedia.mixercontrol, tMIXERCONTROL, tagMIXERCONTROLA, tagMIXERCONTROLW'
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
req.typenames: MIXERCONTROLW, *PMIXERCONTROLW, *LPMIXERCONTROLW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIXERCONTROLW
 - mmeapi/tagMIXERCONTROLW
 - PMIXERCONTROLW
 - mmeapi/PMIXERCONTROLW
 - MIXERCONTROLW
 - mmeapi/MIXERCONTROLW
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
 - MIXERCONTROL, *PMIXERCONTROL, FAR *PMIXERCONTROL
 - mixercontrolw
---

# MIXERCONTROLW structure


## -description

The <b>MIXERCONTROL</b> structure describes the state and metrics of a single control for an audio line.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>MIXERCONTROL</b> structure.

### -field dwControlID

Audio mixer-defined identifier that uniquely refers to the control described by the <b>MIXERCONTROL</b> structure. This identifier can be in any format supported by the mixer device. An application should use this identifier only as an abstract handle. No two controls for a single mixer device can ever have the same control identifier.

### -field dwControlType

Class of the control for which the identifier is specified in <b>dwControlID</b>. An application must use this information to display the appropriate control for input from the user. An application can also display tailored graphics based on the control class or search for a particular control class on a specific line. If an application does not know about a control class, this control must be ignored. There are eight control class classifications, each with one or more standard control types:

<table>
<tr>
<th>Name</th>
<th>Descriptions</th>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_CUSTOM"></a><a id="mixercontrol_ct_class_custom"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_CUSTOM</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_CUSTOM

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_FADER"></a><a id="mixercontrol_ct_class_fader"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_FADER</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_BASS MIXERCONTROL_CONTROLTYPE_EQUALIZER MIXERCONTROL_CONTROLTYPE_FADER MIXERCONTROL_CONTROLTYPE_TREBLE MIXERCONTROL_CONTROLTYPE_VOLUME

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_LIST"></a><a id="mixercontrol_ct_class_list"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_LIST</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_MIXER MIXERCONTROL_CONTROLTYPE_MULTIPLESELECT MIXERCONTROL_CONTROLTYPE_MUX MIXERCONTROL_CONTROLTYPE_SINGLESELECT

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_METER"></a><a id="mixercontrol_ct_class_meter"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_METER</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_BOOLEANMETER MIXERCONTROL_CONTROLTYPE_PEAKMETER MIXERCONTROL_CONTROLTYPE_SIGNEDMETER MIXERCONTROL_CONTROLTYPE_UNSIGNEDMETER

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_NUMBER"></a><a id="mixercontrol_ct_class_number"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_DECIBELS MIXERCONTROL_CONTROLTYPE_PERCENT MIXERCONTROL_CONTROLTYPE_SIGNED MIXERCONTROL_CONTROLTYPE_UNSIGNED

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_SLIDER"></a><a id="mixercontrol_ct_class_slider"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_SLIDER</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_PAN MIXERCONTROL_CONTROLTYPE_QSOUNDPAN MIXERCONTROL_CONTROLTYPE_SLIDER

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_SWITCH"></a><a id="mixercontrol_ct_class_switch"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_SWITCH</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_BOOLEAN MIXERCONTROL_CONTROLTYPE_BUTTON MIXERCONTROL_CONTROLTYPE_LOUDNESS MIXERCONTROL_CONTROLTYPE_MONO MIXERCONTROL_CONTROLTYPE_MUTE MIXERCONTROL_CONTROLTYPE_ONOFF MIXERCONTROL_CONTROLTYPE_STEREOENH

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CT_CLASS_TIME"></a><a id="mixercontrol_ct_class_time"></a><dl>
<dt><b>MIXERCONTROL_CT_CLASS_TIME</b></dt>
</dl>
</td>
<td width="60%">
MIXERCONTROL_CONTROLTYPE_MICROTIME MIXERCONTROL_CONTROLTYPE_MILLITIME

</td>
</tr>
</table>

### -field fdwControl

Status and support flags for the audio line control. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CONTROLF_DISABLED"></a><a id="mixercontrol_controlf_disabled"></a><dl>
<dt><b>MIXERCONTROL_CONTROLF_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The control is disabled, perhaps due to other settings for the mixer hardware, and cannot be used. An application can read current settings from a disabled control, but it cannot apply settings.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CONTROLF_MULTIPLE"></a><a id="mixercontrol_controlf_multiple"></a><dl>
<dt><b>MIXERCONTROL_CONTROLF_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
The control has two or more settings per channel. An equalizer, for example, requires this flag because each frequency band can be set to a different value. An equalizer that affects both channels of a stereo line in a uniform fashion will also specify the MIXERCONTROL_CONTROLF_UNIFORM flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MIXERCONTROL_CONTROLF_UNIFORM"></a><a id="mixercontrol_controlf_uniform"></a><dl>
<dt><b>MIXERCONTROL_CONTROLF_UNIFORM</b></dt>
</dl>
</td>
<td width="60%">
The control acts on all channels of a multichannel line in a uniform fashion. For example, a control that mutes both channels of a stereo line would set this flag. Most MIXERCONTROL_CONTROLTYPE_MUX and MIXERCONTROL_CONTROLTYPE_MIXER controls also specify the MIXERCONTROL_CONTROLF_UNIFORM flag.

</td>
</tr>
</table>

### -field cMultipleItems

Number of items per channel that make up a MIXERCONTROL_CONTROLF_MULTIPLE control. This number is always two or greater for multiple-item controls. If the control is not a multiple-item control, do not use this member; it will be zero.

### -field szShortName

Short string that describes the audio line control specified by <b>dwControlID</b>. This description should be appropriate to use as a concise label for the control.

### -field szName

String that describes the audio line control specified by <b>dwControlID</b>. This description should be appropriate to use as a complete description for the control.

### -field Bounds

Union of boundary types.

### -field Bounds.DUMMYSTRUCTNAME

### -field Bounds.DUMMYSTRUCTNAME.lMinimum

Minimum signed value for a control that has a signed boundary nature. This member cannot be used in conjunction with <b>dwMinimum</b>.

### -field Bounds.DUMMYSTRUCTNAME.lMaximum

Maximum signed value for a control that has a signed boundary nature. This member cannot be used in conjunction with <b>dwMaximum</b>.

### -field Bounds.DUMMYSTRUCTNAME2

### -field Bounds.DUMMYSTRUCTNAME2.dwMinimum

Minimum unsigned value for a control that has an unsigned boundary nature. This member cannot be used in conjunction with <b>lMinimum</b>.

### -field Bounds.DUMMYSTRUCTNAME2.dwMaximum

Maximum unsigned value for a control that has an unsigned boundary nature. This member cannot be used in conjunction with <b>lMaximum</b>.

### -field Bounds.dwReserved

Reserved; do not use.

### -field Metrics

Union of boundary metrics.

### -field Metrics.cSteps

Number of discrete ranges within the union specified for a control specified by the <b>Bounds</b> member. This member overlaps with the other members of the <b>Metrics</b> structure member and cannot be used in conjunction with those members.

### -field Metrics.cbCustomData

Size, in bytes, required to contain the state of a custom control class. This member is appropriate only for the MIXERCONTROL_CONTROLTYPE_CUSTOM control class.

### -field Metrics.dwReserved

Reserved; do not use.

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-structures">Audio Mixer Structures</a>



Audio Mixers



<a href="/windows/desktop/api/mmeapi/ns-mmeapi-mixerlinecontrolsa">MIXERLINECONTROLS</a>



<a href="/previous-versions/dd757302(v=vs.85)">mixerGetLineControls</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines MIXERCONTROL as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
