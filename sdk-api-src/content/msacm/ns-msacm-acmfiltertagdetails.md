---
UID: NS:msacm.tACMFILTERTAGDETAILS
title: ACMFILTERTAGDETAILS (msacm.h)
description: The ACMFILTERTAGDETAILS structure details a waveform-audio filter tag for an ACM filter driver.
helpviewer_keywords: ["*LPACMFILTERTAGDETAILS","*PACMFILTERTAGDETAILS","ACMDRIVERDETAILS_SUPPORTF_ASYNC","ACMDRIVERDETAILS_SUPPORTF_CODEC","ACMDRIVERDETAILS_SUPPORTF_CONVERTER","ACMDRIVERDETAILS_SUPPORTF_FILTER","ACMDRIVERDETAILS_SUPPORTF_HARDWARE","ACMFILTERTAGDETAILS","ACMFILTERTAGDETAILS structure [Windows Multimedia]","msacm/ACMFILTERTAGDETAILS","multimedia.acmfiltertagdetails_COLLISION761","multimedia.acmfiltertagdetails_struct"]
old-location: multimedia\acmfiltertagdetails_struct.htm
tech.root: Multimedia
ms.assetid: 94b31090-74ed-42ac-b904-0a90f055e03a
ms.date: 12/05/2018
ms.keywords: '*LPACMFILTERTAGDETAILS, *PACMFILTERTAGDETAILS, ACMDRIVERDETAILS_SUPPORTF_ASYNC, ACMDRIVERDETAILS_SUPPORTF_CODEC, ACMDRIVERDETAILS_SUPPORTF_CONVERTER, ACMDRIVERDETAILS_SUPPORTF_FILTER, ACMDRIVERDETAILS_SUPPORTF_HARDWARE, ACMFILTERTAGDETAILS, ACMFILTERTAGDETAILS structure [Windows Multimedia], msacm/ACMFILTERTAGDETAILS, multimedia.acmfiltertagdetails_COLLISION761, multimedia.acmfiltertagdetails_struct'
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
req.typenames: ACMFILTERTAGDETAILS, *PACMFILTERTAGDETAILS, *LPACMFILTERTAGDETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMFILTERTAGDETAILS
 - msacm/tACMFILTERTAGDETAILS
 - PACMFILTERTAGDETAILS
 - msacm/PACMFILTERTAGDETAILS
 - ACMFILTERTAGDETAILS
 - msacm/ACMFILTERTAGDETAILS
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
 - ACMFILTERTAGDETAILS
---

# ACMFILTERTAGDETAILS structure


## -description

The <b>ACMFILTERTAGDETAILS</b> structure details a waveform-audio filter tag for an ACM filter driver.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMFILTERTAGDETAILS</b> structure. This member must be initialized before an application calls the <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a> or <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagenum">acmFilterTagEnum</a> function. The size specified in this member must be large enough to contain the base <b>ACMFILTERTAGDETAILS</b> structure. When the <b>acmFilterTagDetails</b> function returns, this member contains the actual size of the information returned. The returned information will never exceed the requested size.

### -field dwFilterTagIndex

Index of the filter tag to retrieve details for. The index ranges from zero to one less than the number of filter tags supported by an ACM driver. The number of filter tags supported by a driver is contained in the [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. The <b>dwFilterTagIndex</b> member is used only when querying filter tag details about a driver by index; otherwise, this member should be zero.

### -field dwFilterTag

Waveform-audio filter tag that the <b>ACMFILTERTAGDETAILS</b> structure describes. This member is used as an input for the ACM_FILTERTAGDETAILSF_FILTERTAG and ACM_FILTERTAGDETAILSF_LARGESTSIZE query flags. This member is always returned if the <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a> function is successful. This member should be set to WAVE_FILTER_UNKNOWN for all other query flags.

### -field cbFilterSize

Largest total size, in bytes, of a waveform-audio filter of the <b>dwFilterTag</b> type. For example, this member will be 40 for WAVE_FILTER_ECHO and 36 for WAVE_FILTER_VOLUME.

### -field fdwSupport

Driver-support flags specific to the filter tag. These flags are identical to the [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. This member can be a combination of the following values and identifies which operations the driver supports with the filter tag:

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
Driver supports asynchronous conversions.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CODEC"></a><a id="acmdriverdetails_supportf_codec"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CODEC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different format tags while using the specified filter tag. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM with the specified filter tag, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CONVERTER"></a><a id="acmdriverdetails_supportf_converter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different formats of the same format tag while using the specified filter tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM with the specified filter tag, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_FILTER"></a><a id="acmdriverdetails_supportf_filter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_HARDWARE"></a><a id="acmdriverdetails_supportf_hardware"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
Driver supports hardware input, output, or both with the specified filter tag through a waveform-audio device. An application should use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.

</td>
</tr>
</table>

### -field cStandardFilters

Number of standard filters of the <b>dwFilterTag</b> type (that is, the combination of all filter characteristics). This value cannot specify all filters supported by the driver.

### -field szFilterTag

String that describes the <b>dwFilterTag</b> type. This string is always returned if the <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a> function is successful.

## -see-also

[ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md)



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagenum">acmFilterTagEnum</a>