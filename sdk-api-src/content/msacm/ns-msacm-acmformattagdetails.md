---
UID: NS:msacm.tACMFORMATTAGDETAILS
title: ACMFORMATTAGDETAILS (msacm.h)
description: The ACMFORMATTAGDETAILS structure details a waveform-audio format tag for an ACM driver.
helpviewer_keywords: ["*LPACMFORMATTAGDETAILS","*PACMFORMATTAGDETAILS","ACMDRIVERDETAILS_SUPPORTF_ASYNC","ACMDRIVERDETAILS_SUPPORTF_CODEC","ACMDRIVERDETAILS_SUPPORTF_CONVERTER","ACMDRIVERDETAILS_SUPPORTF_FILTER","ACMDRIVERDETAILS_SUPPORTF_HARDWARE","ACMFORMATTAGDETAILS","ACMFORMATTAGDETAILS structure [Windows Multimedia]","msacm/ACMFORMATTAGDETAILS","multimedia.acmformattagdetails_COLLISION956","multimedia.acmformattagdetails_struct"]
old-location: multimedia\acmformattagdetails_struct.htm
tech.root: Multimedia
ms.assetid: 134cccb1-4065-407f-a02b-7bd340b4a8cf
ms.date: 12/05/2018
ms.keywords: '*LPACMFORMATTAGDETAILS, *PACMFORMATTAGDETAILS, ACMDRIVERDETAILS_SUPPORTF_ASYNC, ACMDRIVERDETAILS_SUPPORTF_CODEC, ACMDRIVERDETAILS_SUPPORTF_CONVERTER, ACMDRIVERDETAILS_SUPPORTF_FILTER, ACMDRIVERDETAILS_SUPPORTF_HARDWARE, ACMFORMATTAGDETAILS, ACMFORMATTAGDETAILS structure [Windows Multimedia], msacm/ACMFORMATTAGDETAILS, multimedia.acmformattagdetails_COLLISION956, multimedia.acmformattagdetails_struct'
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
req.typenames: ACMFORMATTAGDETAILS, *PACMFORMATTAGDETAILS, *LPACMFORMATTAGDETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMFORMATTAGDETAILS
 - msacm/tACMFORMATTAGDETAILS
 - PACMFORMATTAGDETAILS
 - msacm/PACMFORMATTAGDETAILS
 - ACMFORMATTAGDETAILS
 - msacm/ACMFORMATTAGDETAILS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msacm.h
api_name:
 - ACMFORMATTAGDETAILS
---

# ACMFORMATTAGDETAILS structure


## -description

The <b>ACMFORMATTAGDETAILS</b> structure details a waveform-audio format tag for an ACM driver.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMFORMATTAGDETAILS</b> structure. This member must be initialized before an application calls the <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> or <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagenum">acmFormatTagEnum</a> function. The size specified by this member must be large enough to contain the base <b>ACMFORMATTAGDETAILS</b> structure. When the <b>acmFormatTagDetails</b> function returns, this member contains the actual size of the information returned. The returned information will never exceed the requested size.

### -field dwFormatTagIndex

Index of the format tag for which details will be retrieved. The index ranges from zero to one less than the number of format tags supported by an ACM driver. The number of format tags supported by a driver is contained in the [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. The <b>dwFormatTagIndex</b> member is used only when querying format tag details on a driver by index; otherwise, this member should be zero.

### -field dwFormatTag

Waveform-audio format tag that the <b>ACMFORMATTAGDETAILS</b> structure describes. This member is used for input for the ACM_FORMATTAGDETAILSF_FORMATTAG and ACM_FORMATTAGDETAILSF_LARGESTSIZE query flags. If the <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> function is successful, this member is always returned. This member should be set to WAVE_FORMAT_UNKNOWN for all other query flags.

### -field cbFormatSize

Largest total size, in bytes, of a waveform-audio format of the <b>dwFormatTag</b> type. For example, this member will be 16 for WAVE_FORMAT_PCM and 50 for WAVE_FORMAT_ADPCM.

### -field fdwSupport

Driver-support flags specific to the format tag. These flags are identical to the [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. This member may be some combination of the following values and refer to what operations the driver supports with the format tag:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_ASYNC"></a><a id="acmdriverdetails_supportf_async"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports asynchronous conversions with the specified format tag.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CODEC"></a><a id="acmdriverdetails_supportf_codec"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CODEC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different format tags where one of the tags is the specified format tag. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CONVERTER"></a><a id="acmdriverdetails_supportf_converter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different formats of the specified format tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_FILTER"></a><a id="acmdriverdetails_supportf_filter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on the specified format tag, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_HARDWARE"></a><a id="acmdriverdetails_supportf_hardware"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
Driver supports hardware input, output, or both of the specified format tag through a waveform-audio device. An application should use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.

</td>
</tr>
</table>

### -field cStandardFormats

Number of standard formats of the <b>dwFormatTag</b> type; that is, the combination of all sample rates, bits per sample, channels, and so on. This value can specify all formats supported by the driver, but not necessarily.

### -field szFormatTag

String that describes the <b>dwFormatTag</b> type. If the <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> function is successful, this string is always returned.

## -see-also

[ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md)



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformattagenum">acmFormatTagEnum</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a>