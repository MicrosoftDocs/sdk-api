---
UID: NS:mmeapi.tagWAVEINCAPSA
title: WAVEINCAPSA (mmeapi.h)
description: The WAVEINCAPS structure describes the capabilities of a waveform-audio input device. (WAVEINCAPSA)
helpviewer_keywords: ["*LPWAVEINCAPSA","*NPWAVEINCAPSA","*PWAVEINCAPSA","WAVEINCAPS","WAVEINCAPS structure [Windows Multimedia]","WAVEINCAPSA","_win32_WAVEINCAPS_str","mmeapi/WAVEINCAPS","multimedia.waveincaps","tagWAVEINCAPSA","tagWAVEINCAPSW","waveincaps_tag"]
old-location: multimedia\waveincaps.htm
tech.root: Multimedia
ms.assetid: e96524fd-82d3-4363-989b-23fb20786f3c
ms.date: 12/05/2018
ms.keywords: '*LPWAVEINCAPSA, *NPWAVEINCAPSA, *PWAVEINCAPSA, WAVEINCAPS, WAVEINCAPS structure [Windows Multimedia], WAVEINCAPSA, _win32_WAVEINCAPS_str, mmeapi/WAVEINCAPS, multimedia.waveincaps, tagWAVEINCAPSA, tagWAVEINCAPSW, waveincaps_tag'
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
req.typenames: WAVEINCAPSA, *PWAVEINCAPSA, *NPWAVEINCAPSA, *LPWAVEINCAPSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWAVEINCAPSA
 - mmeapi/tagWAVEINCAPSA
 - PWAVEINCAPSA
 - mmeapi/PWAVEINCAPSA
 - WAVEINCAPSA
 - mmeapi/WAVEINCAPSA
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
 - WAVEINCAPS
 - WAVEINCAPSA
---

# WAVEINCAPSA structure


## -description

The <b>WAVEINCAPS</b> structure describes the capabilities of a waveform-audio input device.

## -struct-fields

### -field wMid

Manufacturer identifier for the device driver for the waveform-audio input device. Manufacturer identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field wPid

Product identifier for the waveform-audio input device. Product identifiers are defined in <a href="/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.

### -field vDriverVersion

Version number of the device driver for the waveform-audio input device. The high-order byte is the major version number, and the low-order byte is the minor version number.

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

Number specifying whether the device supports mono (1) or stereo (2) input.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>

## -remarks

> [!NOTE]
> The mmeapi.h header defines WAVEINCAPS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
