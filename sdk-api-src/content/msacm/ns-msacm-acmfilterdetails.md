---
UID: NS:msacm.tACMFILTERDETAILS
title: ACMFILTERDETAILS (msacm.h)
description: The ACMFILTERDETAILS structure details a waveform-audio filter for a specific filter tag for an ACM driver.
helpviewer_keywords: ["*LPACMFILTERDETAILS","*PACMFILTERDETAILS","ACMDRIVERDETAILS_SUPPORTF_ASYNC","ACMDRIVERDETAILS_SUPPORTF_CODEC","ACMDRIVERDETAILS_SUPPORTF_CONVERTER","ACMDRIVERDETAILS_SUPPORTF_FILTER","ACMDRIVERDETAILS_SUPPORTF_HARDWARE","ACMFILTERDETAILS","ACMFILTERDETAILS structure [Windows Multimedia]","msacm/ACMFILTERDETAILS","multimedia.acmfilterdetails_COLLISION925","multimedia.acmfilterdetails_struct"]
old-location: multimedia\acmfilterdetails_struct.htm
tech.root: Multimedia
ms.assetid: c0423701-b957-4f77-a565-f6f761614389
ms.date: 12/05/2018
ms.keywords: '*LPACMFILTERDETAILS, *PACMFILTERDETAILS, ACMDRIVERDETAILS_SUPPORTF_ASYNC, ACMDRIVERDETAILS_SUPPORTF_CODEC, ACMDRIVERDETAILS_SUPPORTF_CONVERTER, ACMDRIVERDETAILS_SUPPORTF_FILTER, ACMDRIVERDETAILS_SUPPORTF_HARDWARE, ACMFILTERDETAILS, ACMFILTERDETAILS structure [Windows Multimedia], msacm/ACMFILTERDETAILS, multimedia.acmfilterdetails_COLLISION925, multimedia.acmfilterdetails_struct'
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
req.typenames: ACMFILTERDETAILS, *PACMFILTERDETAILS, *LPACMFILTERDETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMFILTERDETAILS
 - msacm/tACMFILTERDETAILS
 - PACMFILTERDETAILS
 - msacm/PACMFILTERDETAILS
 - ACMFILTERDETAILS
 - msacm/ACMFILTERDETAILS
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
 - ACMFILTERDETAILS
---

# ACMFILTERDETAILS structure


## -description

The <b>ACMFILTERDETAILS</b> structure details a waveform-audio filter for a specific filter tag for an ACM driver.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMFILTERDETAILS</b> structure. This member must be initialized before calling the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a> or <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterenum">acmFilterEnum</a> functions. The size specified in this member must be large enough to contain the base <b>ACMFILTERDETAILS</b> structure. When the <b>acmFilterDetails</b> function returns, this member contains the actual size of the information returned. The returned information will never exceed the requested size.

### -field dwFilterIndex

Index of the filter about which details will be retrieved. The index ranges from zero to one less than the number of standard filters supported by an ACM driver for a filter tag. The number of standard filters supported by a driver for a filter tag is contained in the [ACMFILTERTAGDETAILS](./nf-msacm-acmfilterdetails.md) structure. The <b>dwFilterIndex</b> member is used only when querying standard filter details about a driver by index; otherwise, this member should be zero. Also, this member will be set to zero by the ACM when an application queries for details on a filter; in other words, this member is used only for input and is never returned by the ACM or an ACM driver.

### -field dwFilterTag

Waveform-audio filter tag that the <b>ACMFILTERDETAILS</b> structure describes. This member is used as an input for the ACM_FILTERDETAILSF_INDEX query flag. For the ACM_FILTERDETAILSF_FORMAT query flag, this member must be initialized to the same filter tag as the <b>pwfltr</b> member specifies. If the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a> function is successful, this member is always returned. This member should be set to WAVE_FILTER_UNKNOWN for all other query flags.

### -field fdwSupport

Driver-support flags specific to the specified filter. These flags are identical to the [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure, but they are specific to the filter that is being queried. This member can be a combination of the following values and identifies which operations the driver supports for the filter tag:

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
Driver supports conversion between two different format tags while using the specified filter. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM with the specified filter, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CONVERTER"></a><a id="acmdriverdetails_supportf_converter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different formats of the same format tag while using the specified filter. For example, if a driver supports resampling of WAVE_FORMAT_PCM with the specified filter, this flag is set.

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
Driver supports hardware input, output, or both with the specified filter through a waveform-audio device. An application should use the <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to retrieve the waveform-audio device identifiers associated with the supporting ACM driver.

</td>
</tr>
</table>

### -field pwfltr

Pointer to a <a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a> structure that will receive the filter details. This structure requires no initialization by the application unless the ACM_FILTERDETAILSF_FILTER flag is specified with the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a> function. In this case, the <b>dwFilterTag</b> member of the <b>WAVEFILTER</b> structure must be equal to the <b>dwFilterTag</b> member of the <b>ACMFILTERDETAILS</b> structure.

### -field cbwfltr

Size, in bytes, available for <b>pwfltr</b> to receive the filter details. The <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> and <a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a> functions can be used to determine the maximum size required for any filter available for the specified driver (or for all installed ACM drivers).

### -field szFilter

String that describes the filter for the <b>dwFilterTag</b> type. If the <a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a> function is successful, this string is always returned.

## -see-also

[ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md)



[ACMFILTERTAGDETAILS](./nf-msacm-acmfilterdetails.md)



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/windows/desktop/api/mmreg/ns-mmreg-wavefilter">WAVEFILTER</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfilterdetails">acmFilterDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfilterenum">acmFilterEnum</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmfiltertagdetails">acmFilterTagDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a>