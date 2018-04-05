---
UID: NS:mmreg.tWAVEFORMATEX
title: tWAVEFORMATEX
author: windows-driver-content
description: The WAVEFORMATEX structure defines the format of waveform-audio data.
old-location: dshow\waveformatex.htm
old-project: DirectShow
ms.assetid: 4f3bf6fb-b15f-43b3-82f1-e7a8a3007057
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPWAVEFORMATEX, *NPWAVEFORMATEX, *PWAVEFORMATEX, WAVEFORMATEX, WAVEFORMATEX structure [DirectShow], WAVEFORMATEXStructure, dshow.waveformatex, mmreg/WAVEFORMATEX, tWAVEFORMATEX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mmreg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WAVEFORMATEX, WAVEFORMATEX, *PWAVEFORMATEX, *NPWAVEFORMATEX, *LPWAVEFORMATEX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mmreg.h
api_name:
-	WAVEFORMATEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tWAVEFORMATEX structure


## -description



The <b>WAVEFORMATEX</b> structure defines the format of waveform-audio data. Only format information common to all waveform-audio data formats is included in this structure. For formats that require additional information, this structure is included as the first member in another structure, along with the additional information.




## -struct-fields




### -field wFormatTag

Waveform-audio format type. Format tags are registered with Microsoft Corporation for many compression algorithms. A complete list of format tags can be found in the Mmreg.h header file. For one- or two-channel Pulse Code Modulation (PCM) data, this value should be WAVE_FORMAT_PCM.

<ul>
<li>If <b>wFormatTag</b> equals WAVE_FORMAT_EXTENSIBLE, the structure is interpreted as a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538802">WAVEFORMATEXTENSIBLE</a> structure.</li>
<li>If <b>wFormatTag</b> equals WAVE_FORMAT_MPEG, the structure is interpreted as an <a href="https://msdn.microsoft.com/c9357f72-f101-434a-b7ae-183e78239e9c">MPEG1WAVEFORMAT</a> structure.</li>
<li>If <b>wFormatTag</b> equals WAVE_FORMAT_MPEGLAYER3, the structure is interpreted as an <a href="https://msdn.microsoft.com/eca403a0-01a2-4290-951f-a7d516a58b9e">MPEGLAYER3WAVEFORMAT</a> structure.</li>
</ul>
Before reinterpreting a <b>WAVEFORMATEX</b> structure as one of these extended structures, verify that the actual structure size is sufficiently large and that the <b>cbSize</b> member indicates a valid size.


### -field nChannels

Number of channels in the waveform-audio data. Monaural data uses one channel and stereo data uses two channels.


### -field nSamplesPerSec

Sample rate, in samples per second (hertz). If <b>wFormatTag</b> is WAVE_FORMAT_PCM, then common values for <b>nSamplesPerSec</b> are 8.0 kHz, 11.025 kHz, 22.05 kHz, and 44.1 kHz. For non-PCM formats, this member must be computed according to the manufacturer's specification of the format tag.


### -field nAvgBytesPerSec

Required average data-transfer rate, in bytes per second, for the format tag. If <b>wFormatTag</b> is WAVE_FORMAT_PCM, <b>nAvgBytesPerSec</b> must equal <b>nSamplesPerSec</b> × <b>nBlockAlign</b>. For non-PCM formats, this member must be computed according to the manufacturer's specification of the format tag.


### -field nBlockAlign

Block alignment, in bytes. The block alignment is the minimum atomic unit of data for the <b>wFormatTag</b> format type. If <b>wFormatTag</b> is WAVE_FORMAT_PCM, <b>nBlockAlign</b> must equal (<b>nChannels</b> × <b>wBitsPerSample</b>) / 8. For non-PCM formats, this member must be computed according to the manufacturer's specification of the format tag.

Software must process a multiple of <b>nBlockAlign</b> bytes of data at a time. Data written to and read from a device must always start at the beginning of a block. For example, it is illegal to start playback of PCM data in the middle of a sample (that is, on a non-block-aligned boundary). 


### -field wBitsPerSample

Bits per sample for the <b>wFormatTag</b> format type. If <b>wFormatTag</b> is <b>WAVE_FORMAT_PCM</b>, then <b>wBitsPerSample</b> should be equal to 8 or 16. For non-PCM formats, this member must be set according to the manufacturer's specification of the format tag. If <b>wFormatTag</b> is <b>WAVE_FORMAT_EXTENSIBLE</b>, this value can be any integer multiple of 8. 

Some compression schemes do not define a value for <b>wBitsPerSample</b>, so this member can be zero.


### -field cbSize


            Size, in bytes, of extra format information appended to the end of the <b>WAVEFORMATEX</b> structure. This information can be used by non-PCM formats to store extra attributes for the <b>wFormatTag</b>. If no extra information is required by the <b>wFormatTag</b>, this member must be set to zero. For <b>WAVE_FORMAT_PCM</b> formats (and only <b>WAVE_FORMAT_PCM</b> formats), this member is ignored. However it is still recommended to set the value.
          


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/b16cdcab-fa4f-4c9a-b1f3-af459bd33245">WAVEFORMATEXTENSIBLE Structure</a>
 

 

