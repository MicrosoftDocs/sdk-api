---
UID: NS:mmeapi.waveincaps_tag
title: WAVEINCAPS (mmeapi.h)
author: windows-sdk-content
description: The WAVEINCAPS structure describes the capabilities of a waveform-audio input device.
old-location: multimedia\waveincaps.htm
tech.root: Multimedia
ms.assetid: e96524fd-82d3-4363-989b-23fb20786f3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPWAVEINCAPS, *NPWAVEINCAPS, *PWAVEINCAPS, WAVEINCAPS, WAVEINCAPS structure [Windows Multimedia], _win32_WAVEINCAPS_str, mmeapi/WAVEINCAPS, multimedia.waveincaps, tagWAVEINCAPSA, tagWAVEINCAPSW, waveincaps_tag"
ms.topic: struct
f1_keywords: 
 - "mmeapi/WAVEINCAPS"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - WAVEINCAPS
targetos: Windows
req.typenames: WAVEINCAPS, *PWAVEINCAPS, *NPWAVEINCAPS, *LPWAVEINCAPS
req.redist: 
ms.custom: 19H1
---

# WAVEINCAPS structure


## -description



The <b>WAVEINCAPS</b> structure describes the capabilities of a waveform-audio input device.




## -struct-fields




### -field wMid

Manufacturer identifier for the device driver for the waveform-audio input device. Manufacturer identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


### -field wPid

Product identifier for the waveform-audio input device. Product identifiers are defined in <a href="https://docs.microsoft.com/windows/desktop/Multimedia/manufacturer-and-product-identifiers">Manufacturer and Product Identifiers</a>.


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


#### - wReserved1

Padding.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>
 

 

