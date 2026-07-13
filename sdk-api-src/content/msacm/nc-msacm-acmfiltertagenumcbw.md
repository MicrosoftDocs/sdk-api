---
UID: NC:msacm.ACMFILTERTAGENUMCBW
title: ACMFILTERTAGENUMCBW (msacm.h)
description: The ACMFILTERTAGENUMCBW (Unicode) callback function specifies a callback function used with the acmFilterTagEnum function.
helpviewer_keywords: ["ACMFILTERTAGENUMCB","ACMFILTERTAGENUMCB callback","ACMFILTERTAGENUMCBA","ACMFILTERTAGENUMCBW","_win32_acmFilterTagEnumCallback","acmFilterTagEnumCallback","acmFilterTagEnumCallback callback function [Windows Multimedia]","msacm/ACMFILTERTAGENUMCBA","msacm/ACMFILTERTAGENUMCBW","msacm/acmFilterTagEnumCallback","multimedia.acmfiltertagenumcallback"]
old-location: multimedia\acmfiltertagenumcallback.htm
tech.root: Multimedia
ms.assetid: 63469be1-d657-4e95-9978-d31140ccd46f
ms.date: 08/02/2022
ms.keywords: ACMFILTERTAGENUMCB, ACMFILTERTAGENUMCB callback, ACMFILTERTAGENUMCBA, ACMFILTERTAGENUMCBW, _win32_acmFilterTagEnumCallback, acmFilterTagEnumCallback, acmFilterTagEnumCallback callback function [Windows Multimedia], msacm/ACMFILTERTAGENUMCBA, msacm/ACMFILTERTAGENUMCBW, msacm/acmFilterTagEnumCallback, multimedia.acmfiltertagenumcallback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ACMFILTERTAGENUMCBW
 - msacm/ACMFILTERTAGENUMCBW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - acmFilterTagEnumCallback
 - ACMFILTERTAGENUMCBA
 - ACMFILTERTAGENUMCBW
---

# ACMFILTERTAGENUMCBW callback function


## -description

The <b>acmFilterTagEnumCallback</b> function specifies a callback function used with the <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagenum">acmFilterTagEnum</a> function. The <b>acmFilterTagEnumCallback</b> function name is a placeholder for an application-defined function name.

## -parameters

### -param hadid

Handle to the ACM driver identifier.

### -param paftd

Pointer to an [ACMFILTERTAGDETAILS](./nf-msacm-acmfiltertagdetails.md) structure that contains the enumerated filter tag details.

### -param dwInstance

Application-defined value specified in <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagenum">acmFilterTagEnum</a>.

### -param fdwSupport

Driver-support flags specific to the driver identifier [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. This parameter can be a combination of the following values and identifies which operations the driver supports with the filter tag.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_ASYNC</b></td>
<td>Driver supports asynchronous conversions with the specified filter tag.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_CODEC</b></td>
<td>Driver supports conversion between two different format tags while using the specified filter tag. For example, if a driver supports compression from <b>WAVE_FORMAT_PCM</b> to <b>WAVE_FORMAT_ADPCM</b> with the specified filter tag, this flag is set.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></td>
<td>Driver supports conversion between two different formats of the same format tag while using the specified filter tag. For example, if a driver supports resampling of <b>WAVE_FORMAT_PCM</b> with the specified filter tag, this flag is set.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on <b>WAVE_FORMAT_PCM</b>, this flag is set.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></td>
<td>Driver supports hardware input, output, or both with the specified filter tag through a waveform-audio device. An application should use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> function with the <b>ACM_METRIC_HARDWARE_WAVE_INPUT</b> and <b>ACM_METRIC_HARDWARE_WAVE_OUTPUT</b> metric indices to get the waveform-audio device identifiers associated with the supporting ACM driver.</td>
</tr>
</table>

## -returns

The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.

## -remarks

The <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagenum">acmFilterTagEnum</a> function returns <b>MMSYSERR_NOERROR</b> (zero) if no filter tags are to be enumerated. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="/windows/desktop/api/msacm/nf-msacm-acmdriveradd">acmDriverAdd</a>, <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverremove">acmDriverRemove</a>, and <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverpriority">acmDriverPriority</a>.





> [!NOTE]
> The msacm.h header defines ACMFILTERTAGENUMCB as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
