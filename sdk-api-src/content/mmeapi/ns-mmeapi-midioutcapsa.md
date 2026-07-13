---
UID: NS:mmeapi.tagMIDIOUTCAPSA
title: MIDIOUTCAPSA (mmeapi.h)
description: The MIDIOUTCAPS structure describes the capabilities of a MIDI output device. (MIDIOUTCAPSA)
helpviewer_keywords: ["*LPMIDIOUTCAPSA","*NPMIDIOUTCAPSA","*PMIDIOUTCAPSA","MIDICAPS_CACHE","MIDICAPS_LRVOLUME","MIDICAPS_STREAM","MIDICAPS_VOLUME","MIDIOUTCAPS","MIDIOUTCAPS structure [Windows Multimedia]","MIDIOUTCAPSA","MOD_FMSYNTH","MOD_MAPPER","MOD_MIDIPORT","MOD_SQSYNTH","MOD_SWSYNTH","MOD_SYNTH","MOD_WAVETABLE","_win32_MIDIOUTCAPS_str","midioutcaps_tag","mmeapi/MIDIOUTCAPS","multimedia.midioutcaps","tagMIDIOUTCAPSA","tagMIDIOUTCAPSW"]
old-location: multimedia\midioutcaps.htm
tech.root: Multimedia
ms.assetid: 395d5fc2-cf34-48f0-a0b0-185247309e2c
ms.date: 12/05/2018
ms.keywords: '*LPMIDIOUTCAPSA, *NPMIDIOUTCAPSA, *PMIDIOUTCAPSA, MIDICAPS_CACHE, MIDICAPS_LRVOLUME, MIDICAPS_STREAM, MIDICAPS_VOLUME, MIDIOUTCAPS, MIDIOUTCAPS structure [Windows Multimedia], MIDIOUTCAPSA, MOD_FMSYNTH, MOD_MAPPER, MOD_MIDIPORT, MOD_SQSYNTH, MOD_SWSYNTH, MOD_SYNTH, MOD_WAVETABLE, _win32_MIDIOUTCAPS_str, midioutcaps_tag, mmeapi/MIDIOUTCAPS, multimedia.midioutcaps, tagMIDIOUTCAPSA, tagMIDIOUTCAPSW'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIDIOUTCAPSA, *PMIDIOUTCAPSA, *NPMIDIOUTCAPSA, *LPMIDIOUTCAPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMIDIOUTCAPSA
 - mmeapi/tagMIDIOUTCAPSA
 - PMIDIOUTCAPSA
 - mmeapi/PMIDIOUTCAPSA
 - MIDIOUTCAPSA
 - mmeapi/MIDIOUTCAPSA
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
 - MIDIOUTCAPS
 - MIDIOUTCAPSA
---

# MIDIOUTCAPSA structure


## -description

The <b>MIDIOUTCAPS</b> structure describes the capabilities of a MIDI output device.

## -struct-fields

### -field wMid

Manufacturer identifier of the device driver for the MIDI output device. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

Product identifier of the MIDI output device. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field vDriverVersion

Version number of the device driver for the MIDI output device. The high-order byte is the major version number, and the low-order byte is the minor version number.

### -field szPname

Product name in a null-terminated string.

### -field wTechnology

Type of the MIDI output device. This value can be one of the following:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MOD_MIDIPORT"></a><a id="mod_midiport"></a><dl>
<dt><b>MOD_MIDIPORT</b></dt>
</dl>
</td>
<td width="60%">
MIDI hardware port.

</td>
</tr>
<tr>
<td width="40%"><a id="MOD_SYNTH"></a><a id="mod_synth"></a><dl>
<dt><b>MOD_SYNTH</b></dt>
</dl>
</td>
<td width="60%">
Synthesizer.

</td>
</tr>
<tr>
<td width="40%"><a id="MOD_SQSYNTH"></a><a id="mod_sqsynth"></a><dl>
<dt><b>MOD_SQSYNTH</b></dt>
</dl>
</td>
<td width="60%">
Square wave synthesizer.

</td>
</tr>
<tr>
<td width="40%"><a id="MOD_FMSYNTH"></a><a id="mod_fmsynth"></a><dl>
<dt><b>MOD_FMSYNTH</b></dt>
</dl>
</td>
<td width="60%">
FM synthesizer.

</td>
</tr>
<tr>
<td width="40%"><a id="MOD_MAPPER"></a><a id="mod_mapper"></a><dl>
<dt><b>MOD_MAPPER</b></dt>
</dl>
</td>
<td width="60%">
Microsoft MIDI mapper.

</td>
</tr>
<tr>
<td width="40%"><a id="MOD_WAVETABLE"></a><a id="mod_wavetable"></a><dl>
<dt><b>MOD_WAVETABLE</b></dt>
</dl>
</td>
<td width="60%">
Hardware wavetable synthesizer.

</td>
</tr>
<tr>
<td width="40%"><a id="MOD_SWSYNTH"></a><a id="mod_swsynth"></a><dl>
<dt><b>MOD_SWSYNTH</b></dt>
</dl>
</td>
<td width="60%">
Software synthesizer.

</td>
</tr>
</table>

### -field wVoices

Number of voices supported by an internal synthesizer device. If the device is a port, this member is not meaningful and is set to 0.

### -field wNotes

Maximum number of simultaneous notes that can be played by an internal synthesizer device. If the device is a port, this member is not meaningful and is set to 0.

### -field wChannelMask

Channels that an internal synthesizer device responds to, where the least significant bit refers to channel 0 and the most significant bit to channel 15. Port devices that transmit on all channels set this member to 0xFFFF.

### -field dwSupport

Optional functionality supported by the device. It can be one or more of the following:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MIDICAPS_CACHE"></a><a id="midicaps_cache"></a><dl>
<dt><b>MIDICAPS_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Supports patch caching.

</td>
</tr>
<tr>
<td width="40%"><a id="MIDICAPS_LRVOLUME"></a><a id="midicaps_lrvolume"></a><dl>
<dt><b>MIDICAPS_LRVOLUME</b></dt>
</dl>
</td>
<td width="60%">
Supports separate left and right volume control.

</td>
</tr>
<tr>
<td width="40%"><a id="MIDICAPS_STREAM"></a><a id="midicaps_stream"></a><dl>
<dt><b>MIDICAPS_STREAM</b></dt>
</dl>
</td>
<td width="60%">
Provides direct support for the <a href="/previous-versions/dd798487(v=vs.85)">midiStreamOut</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="MIDICAPS_VOLUME"></a><a id="midicaps_volume"></a><dl>
<dt><b>MIDICAPS_VOLUME</b></dt>
</dl>
</td>
<td width="60%">
Supports volume control.

</td>
</tr>
</table>
 

If a device supports volume changes, the MIDICAPS_VOLUME flag will be set for the dwSupport member. If a device supports separate volume changes on the left and right channels, both the MIDICAPS_VOLUME and the MIDICAPS_LRVOLUME flags will be set for this member.

## -see-also

<a href="/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>



<a href="/previous-versions/dd798487(v=vs.85)">midiStreamOut</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines MIDIOUTCAPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
