---
UID: NS:mmeapi.tagWAVEOUTCAPSA
title: WAVEOUTCAPSA (mmeapi.h)
description: The WAVEOUTCAPS structure describes the capabilities of a waveform-audio output device. (WAVEOUTCAPSA)
helpviewer_keywords: ["*LPWAVEOUTCAPSA","*NPWAVEOUTCAPSA","*PWAVEOUTCAPSA","WAVEOUTCAPS","WAVEOUTCAPS structure [Windows Multimedia]","WAVEOUTCAPSA","_win32_WAVEOUTCAPS_str","mmeapi/WAVEOUTCAPS","multimedia.waveoutcaps","tagWAVEOUTCAPSA","tagWAVEOUTCAPSW","waveoutcaps_tag"]
old-location: multimedia\waveoutcaps.htm
tech.root: Multimedia
ms.assetid: 756f47fa-c0d1-4729-a0f6-096a1212d0a2
ms.date: 12/05/2018
ms.keywords: '*LPWAVEOUTCAPSA, *NPWAVEOUTCAPSA, *PWAVEOUTCAPSA, WAVEOUTCAPS, WAVEOUTCAPS structure [Windows Multimedia], WAVEOUTCAPSA, _win32_WAVEOUTCAPS_str, mmeapi/WAVEOUTCAPS, multimedia.waveoutcaps, tagWAVEOUTCAPSA, tagWAVEOUTCAPSW, waveoutcaps_tag'
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
req.typenames: WAVEOUTCAPSA, *PWAVEOUTCAPSA, *NPWAVEOUTCAPSA, *LPWAVEOUTCAPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWAVEOUTCAPSA
 - mmeapi/tagWAVEOUTCAPSA
 - PWAVEOUTCAPSA
 - mmeapi/PWAVEOUTCAPSA
 - WAVEOUTCAPSA
 - mmeapi/WAVEOUTCAPSA
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
 - WAVEOUTCAPS
 - WAVEOUTCAPSA
---

# WAVEOUTCAPSA structure


## -description

The <b>WAVEOUTCAPS</b> structure describes the capabilities of a waveform-audio output device.

## -struct-fields

### -field wMid

Manufacturer identifier for the device driver for the device. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

Product identifier for the device. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field vDriverVersion

Version number of the device driver for the device. The high-order byte is the major version number, and the low-order byte is the minor version number.

### -field szPname

Product name in a null-terminated string.

### -field dwFormats

Standard formats that are supported. Can be a combination of the following:

<table>
<tr>
<th>Format</th>
<th>Description</th>
</tr>
<tr>
<td>WAVE_FORMAT_1M08</td>
<td>11.025 kHz, mono, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_1M16</td>
<td>11.025 kHz, mono, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_1S08</td>
<td>11.025 kHz, stereo, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_1S16</td>
<td>11.025 kHz, stereo, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_2M08</td>
<td>22.05 kHz, mono, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_2M16</td>
<td>22.05 kHz, mono, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_2S08</td>
<td>22.05 kHz, stereo, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_2S16</td>
<td>22.05 kHz, stereo, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_4M08</td>
<td>44.1 kHz, mono, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_4M16</td>
<td>44.1 kHz, mono, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_4S08</td>
<td>44.1 kHz, stereo, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_4S16</td>
<td>44.1 kHz, stereo, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_96M08</td>
<td>96 kHz, mono, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_96M16</td>
<td>96 kHz, mono, 16-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_96S08</td>
<td>96 kHz, stereo, 8-bit</td>
</tr>
<tr>
<td>WAVE_FORMAT_96S16</td>
<td>96 kHz, stereo, 16-bit</td>
</tr>
</table>

### -field wChannels

Number specifying whether the device supports mono (1) or stereo (2) output.

### -field dwSupport

Optional functionality supported by the device. The following values are defined:

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>WAVECAPS_LRVOLUME</td>
<td>Supports separate left and right volume control.</td>
</tr>
<tr>
<td>WAVECAPS_PITCH</td>
<td>Supports pitch control.</td>
</tr>
<tr>
<td>WAVECAPS_PLAYBACKRATE</td>
<td>Supports playback rate control.</td>
</tr>
<tr>
<td>WAVECAPS_SYNC</td>
<td>The driver is synchronous and will block while playing a buffer.</td>
</tr>
<tr>
<td>WAVECAPS_VOLUME</td>
<td>Supports volume control.</td>
</tr>
<tr>
<td>WAVECAPS_SAMPLEACCURATE</td>
<td>Returns sample-accurate position information.</td>
</tr>
</table>

## -remarks

If a device supports volume changes, the WAVECAPS_VOLUME flag will be set for the <b>dwSupport</b> member. If a device supports separate volume changes on the left and right channels, both the WAVECAPS_VOLUME and the WAVECAPS_LRVOLUME flags will be set for this member.





> [!NOTE]
> The mmeapi.h header defines WAVEOUTCAPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>
