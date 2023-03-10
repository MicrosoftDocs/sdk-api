---
UID: NS:mmeapi.tWAVEFORMATEX
title: WAVEFORMATEX (mmeapi.h)
description: The WAVEFORMATEX structure defines the format of waveform-audio data.
helpviewer_keywords: ["*LPWAVEFORMATEX","*NPWAVEFORMATEX","*PWAVEFORMATEX","WAVEFORMATEX","WAVEFORMATEX structure [Windows Multimedia]","_win32_WAVEFORMATEX_str","mmeapi/WAVEFORMATEX","multimedia.waveformatex","tWAVEFORMATEX","tWAVEFORMATEX structure [Windows Multimedia]"]
old-location: multimedia\waveformatex.htm
tech.root: Multimedia
ms.assetid: bd0f96ec-d26a-4e6f-8802-50e8ff207f54
ms.date: 12/05/2018
ms.keywords: '*LPWAVEFORMATEX, *NPWAVEFORMATEX, *PWAVEFORMATEX, WAVEFORMATEX, WAVEFORMATEX structure [Windows Multimedia], _win32_WAVEFORMATEX_str, mmeapi/WAVEFORMATEX, multimedia.waveformatex, tWAVEFORMATEX, tWAVEFORMATEX structure [Windows Multimedia]'
req.header: mmeapi.h
req.include-header: Mmreg.h
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
req.typenames: WAVEFORMATEX, *PWAVEFORMATEX, *NPWAVEFORMATEX, *LPWAVEFORMATEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tWAVEFORMATEX
 - mmeapi/tWAVEFORMATEX
 - PWAVEFORMATEX
 - mmeapi/PWAVEFORMATEX
 - WAVEFORMATEX
 - mmeapi/WAVEFORMATEX
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
 - WAVEFORMATEX
---

# WAVEFORMATEX structure


## -description

The <b>WAVEFORMATEX</b> structure defines the format of waveform-audio data. Only format information common to all waveform-audio data formats is included in this structure. For formats that require additional information, this structure is included as the first member in another structure, along with the additional information.

Formats that support more than two channels or sample sizes of more than 16 bits can be described in a <a href="/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible">WAVEFORMATEXTENSIBLE</a> structure, which includes the <a href="/windows/win32/api/mmeapi/ns-mmeapi-waveformatex">WAVEFORMAT</a> structure.

## -struct-fields

### -field wFormatTag

Waveform-audio format type. Format tags are registered with Microsoft Corporation for many compression algorithms. A complete list of format tags can be found in the Mmreg.h header file. For one- or two-channel PCM data, this value should be WAVE_FORMAT_PCM. When this structure is included in a <a href="/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible">WAVEFORMATEXTENSIBLE</a> structure, this value must be WAVE_FORMAT_EXTENSIBLE.

### -field nChannels

Number of channels in the waveform-audio data. Monaural data uses one channel and stereo data uses two channels.

### -field nSamplesPerSec

Sample rate, in samples per second (hertz). If <b>wFormatTag</b> is WAVE_FORMAT_PCM, then common values for <b>nSamplesPerSec</b> are 8.0 kHz, 11.025 kHz, 22.05 kHz, and 44.1 kHz. For non-PCM formats, this member must be computed according to the manufacturer's specification of the format tag.

### -field nAvgBytesPerSec

Required average data-transfer rate, in bytes per second, for the format tag. If <b>wFormatTag</b> is WAVE_FORMAT_PCM, <b>nAvgBytesPerSec</b> should be equal to the product of <b>nSamplesPerSec</b> and <b>nBlockAlign</b>. For non-PCM formats, this member must be computed according to the manufacturer's specification of the format tag.

### -field nBlockAlign

Block alignment, in bytes. The block alignment is the minimum atomic unit of data for the <b>wFormatTag</b> format type. If <b>wFormatTag</b> is WAVE_FORMAT_PCM or WAVE_FORMAT_EXTENSIBLE, <b>nBlockAlign</b> must be equal to the product of <b>nChannels</b> and <b>wBitsPerSample</b> divided by 8 (bits per byte). For non-PCM formats, this member must be computed according to the manufacturer's specification of the format tag.

Software must process a multiple of <b>nBlockAlign</b> bytes of data at a time. Data written to and read from a device must always start at the beginning of a block. For example, it is illegal to start playback of PCM data in the middle of a sample (that is, on a non-block-aligned boundary).

### -field wBitsPerSample

Bits per sample for the <b>wFormatTag</b> format type. If <b>wFormatTag</b> is WAVE_FORMAT_PCM, then <b>wBitsPerSample</b> should be equal to 8 or 16. For non-PCM formats, this member must be set according to the manufacturer's specification of the format tag. If <b>wFormatTag</b> is WAVE_FORMAT_EXTENSIBLE, this value can be any integer multiple of 8 and represents the container size, not necessarily the sample size; for example, a 20-bit sample size is in a 24-bit container. Some compression schemes cannot define a value for <b>wBitsPerSample</b>, so this member can be 0.

### -field cbSize

Size, in bytes, of extra format information appended to the end of the <b>WAVEFORMATEX</b> structure. This information can be used by non-PCM formats to store extra attributes for the <b>wFormatTag</b>. If no extra information is required by the <b>wFormatTag</b>, this member must be set to 0. For WAVE_FORMAT_PCM formats (and only WAVE_FORMAT_PCM formats), this member is ignored. When this structure is included in a <a href="/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible">WAVEFORMATEXTENSIBLE</a> structure, this value must be at least 22.

## -remarks

An example of a format that uses extra information is the Microsoft Adaptive Delta Pulse Code Modulation (MS-ADPCM) format. The <b>wFormatTag</b> for MS-ADPCM is WAVE_FORMAT_ADPCM. The <b>cbSize</b> member will typically be set to 32. The extra information stored for WAVE_FORMAT_ADPCM is coefficient pairs required for encoding and decoding the waveform-audio data.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-structures">Waveform Structures</a>