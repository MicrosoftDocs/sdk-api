---
UID: NC:msacm.ACMFORMATENUMCBA
title: ACMFORMATENUMCBA (msacm.h)
description: The acmFormatEnumCallback function specifies a callback function used with the acmFormatEnum function. The acmFormatEnumCallback name is a placeholder for the application-defined function name. (ACMFORMATENUMCBA)
helpviewer_keywords: ["ACMFORMATENUMCB","ACMFORMATENUMCB callback","ACMFORMATENUMCB callback function [Windows Multimedia]","ACMFORMATENUMCBA","ACMFORMATENUMCBW","_win32_acmFormatEnumCallback","acmFormatEnumCallback","msacm/ACMFORMATENUMCB","msacm/ACMFORMATENUMCBA","msacm/ACMFORMATENUMCBW","multimedia.acmformatenumcallback"]
old-location: multimedia\acmformatenumcallback.htm
tech.root: Multimedia
ms.assetid: 58775258-c42c-4d59-8922-c478b5bdf0d7
ms.date: 12/05/2018
ms.keywords: ACMFORMATENUMCB, ACMFORMATENUMCB callback, ACMFORMATENUMCB callback function [Windows Multimedia], ACMFORMATENUMCBA, ACMFORMATENUMCBW, _win32_acmFormatEnumCallback, acmFormatEnumCallback, msacm/ACMFORMATENUMCB, msacm/ACMFORMATENUMCBA, msacm/ACMFORMATENUMCBW, multimedia.acmformatenumcallback
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
 - ACMFORMATENUMCBA
 - msacm/ACMFORMATENUMCBA
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
 - ACMFORMATENUMCB
 - ACMFORMATENUMCBA
 - ACMFORMATENUMCBW
---

# ACMFORMATENUMCBA callback function


## -description

The <b>acmFormatEnumCallback</b> function specifies a callback function used with the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a> function. The <b>acmFormatEnumCallback</b> name is a placeholder for the application-defined function name.

## -parameters

### -param hadid

Handle to the ACM driver identifier.

### -param pafd

Pointer to an [ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure that contains the enumerated format details for a format tag.

### -param dwInstance

Application-defined value specified in the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a> function.

### -param fdwSupport

Driver support flags specific to the driver identified by [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure, but they are specific to the format that is being enumerated. This parameter can be a combination of the following values and indicates which operations the driver supports for the format tag.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_ASYNC</td>
<td>Driver supports asynchronous conversions with the specified filter tag.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CODEC</td>
<td>Driver supports conversion between two different format tags for the specified format. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM with the specified format, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</td>
<td>Driver supports conversion between two different formats of the same format tag while using the specified format. For example, if a driver supports resampling of WAVE_FORMAT_PCM to the specified format, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_FILTER</td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes) with the specified format. For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</td>
<td>Driver supports hardware input, output, or both of the specified format tags through a waveform-audio device. An application should use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.</td>
</tr>
</table>

## -returns

The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.

## -remarks

The <a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a> function will return MMSYSERR_NOERROR (zero) if no formats are to be enumerated. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="/windows/desktop/api/msacm/nf-msacm-acmdriveradd">acmDriverAdd</a>, <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverremove">acmDriverRemove</a>, and <a href="/windows/desktop/api/msacm/nf-msacm-acmdriverpriority">acmDriverPriority</a>.





> [!NOTE]
> The msacm.h header defines ACMFORMATENUMCB as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
