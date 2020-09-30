---
UID: NF:msacm.acmFormatSuggest
title: acmFormatSuggest function (msacm.h)
description: The acmFormatSuggest function queries the ACM or a specified ACM driver to suggest a destination format for the supplied source format.
helpviewer_keywords: ["_win32_acmFormatSuggest","acmFormatSuggest","acmFormatSuggest function [Windows Multimedia]","msacm/acmFormatSuggest","multimedia.acmformatsuggest"]
old-location: multimedia\acmformatsuggest.htm
tech.root: Multimedia
ms.assetid: c7618d7e-e41e-4513-9511-2133ef5a1582
ms.date: 12/05/2018
ms.keywords: _win32_acmFormatSuggest, acmFormatSuggest, acmFormatSuggest function [Windows Multimedia], msacm/acmFormatSuggest, multimedia.acmformatsuggest
req.header: msacm.h
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmFormatSuggest
 - msacm/acmFormatSuggest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmFormatSuggest
---

# acmFormatSuggest function


## -description

The <b>acmFormatSuggest</b> function queries the ACM or a specified ACM driver to suggest a destination format for the supplied source format. For example, an application can use this function to determine one or more valid PCM formats to which a compressed format can be decompressed.

## -parameters

### -param had

Handle to an open instance of a driver to query for a suggested destination format. If this parameter is <b>NULL</b>, the ACM attempts to find the best driver to suggest a destination format.

### -param pwfxSrc

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that identifies the source format for which a destination format will be suggested by the ACM or specified driver.

### -param pwfxDst

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that will receive the suggested destination format for the <i>pwfxSrc</i> format. Depending on the <i>fdwSuggest</i> parameter, some members of the structure pointed to by <i>pwfxDst</i> may require initialization.

### -param cbwfxDst

Size, in bytes, available for the destination format. The <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> and <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> functions can be used to determine the maximum size required for any format available for the specified driver (or for all installed ACM drivers).

### -param fdwSuggest

Flags for matching the desired destination format. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_NCHANNELS</td>
<td>The <b>nChannels</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>nChannels</b> or fail.</td>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_NSAMPLESPERSEC</td>
<td>The <b>nSamplesPerSec</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>nSamplesPerSec</b> or fail.</td>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_WBITSPERSAMPLE</td>
<td>The <b>wBitsPerSample</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>wBitsPerSample</b> or fail.</td>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_WFORMATTAG</td>
<td>The <b>wFormatTag</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>wFormatTag</b> or fail.</td>
</tr>
</table>

## -returns

Returns zero if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
At least one flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>