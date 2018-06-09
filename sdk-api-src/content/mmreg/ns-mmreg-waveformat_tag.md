---
UID: NS:mmreg.waveformat_tag
title: waveformat_tag
author: windows-sdk-content
description: The WAVEFORMAT structure describes the format of waveform-audio data. Only format information common to all waveform-audio data formats is included in this structure. This structure has been superseded by the WAVEFORMATEX structure.
old-location: multimedia\waveformat.htm
old-project: Multimedia
ms.assetid: 48871868-792a-4479-9e92-95306c25673a
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*LPWAVEFORMAT, *NPWAVEFORMAT, *PWAVEFORMAT, WAVEFORMAT, WAVEFORMAT structure [Windows Multimedia], WAVE_FORMAT_PCM, _win32_WAVEFORMAT_str, mmeapi/WAVEFORMAT, multimedia.waveformat, tWAVEFORMATEX, waveformat_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmreg.h
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
tech.root: 
req.typenames: WAVEFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - WAVEFORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# waveformat_tag structure


## -description



The <b>WAVEFORMAT</b> structure describes the format of waveform-audio data. Only format information common to all waveform-audio data formats is included in this structure. This structure has been superseded by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure.




## -struct-fields




### -field wFormatTag

Format type. The following type is defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="WAVE_FORMAT_PCM"></a><a id="wave_format_pcm"></a><dl>
<dt><b>WAVE_FORMAT_PCM</b></dt>
</dl>
</td>
<td width="60%">
Waveform-audio data is PCM.

</td>
</tr>
</table>
 


### -field nChannels

Number of channels in the waveform-audio data. Mono data uses one channel and stereo data uses two channels.


### -field nSamplesPerSec

Sample rate, in samples per second.


### -field nAvgBytesPerSec

Required average data transfer rate, in bytes per second. For example, 16-bit stereo at 44.1 kHz has an average data rate of 176,400 bytes per second (2 channels — 2 bytes per sample per channel — 44,100 samples per second).


### -field nBlockAlign

Block alignment, in bytes. The block alignment is the minimum atomic unit of data. For PCM data, the block alignment is the number of bytes used by a single sample, including data for both channels if the data is stereo. For example, the block alignment for 16-bit stereo PCM is 4 bytes (2 channels — 2 bytes per sample).


## -remarks



For formats that require additional information, this structure is included as a member in another structure along with the additional information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>



<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/4ae84ba8-f444-4d9e-adc8-343b4ee764cc">Waveform Structures</a>
 

 

