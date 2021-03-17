---
UID: NS:msacm.tACMFORMATDETAILS
title: ACMFORMATDETAILS (msacm.h)
description: The ACMFORMATDETAILS structure details a waveform-audio format for a specific format tag for an ACM driver.
helpviewer_keywords: ["*LPACMFORMATDETAILS","*PACMFORMATDETAILS","ACMDRIVERDETAILS_SUPPORTF_ASYNC","ACMDRIVERDETAILS_SUPPORTF_CODEC","ACMDRIVERDETAILS_SUPPORTF_CONVERTER","ACMDRIVERDETAILS_SUPPORTF_FILTER","ACMDRIVERDETAILS_SUPPORTF_HARDWARE","ACMFORMATDETAILS","ACMFORMATDETAILS structure [Windows Multimedia]","msacm/ACMFORMATDETAILS","multimedia.acmformatdetails_COLLISION956","multimedia.acmformatdetails_struct"]
old-location: multimedia\acmformatdetails_struct.htm
tech.root: Multimedia
ms.assetid: a0760541-c083-447d-a812-dd7f05afb622
ms.date: 12/05/2018
ms.keywords: '*LPACMFORMATDETAILS, *PACMFORMATDETAILS, ACMDRIVERDETAILS_SUPPORTF_ASYNC, ACMDRIVERDETAILS_SUPPORTF_CODEC, ACMDRIVERDETAILS_SUPPORTF_CONVERTER, ACMDRIVERDETAILS_SUPPORTF_FILTER, ACMDRIVERDETAILS_SUPPORTF_HARDWARE, ACMFORMATDETAILS, ACMFORMATDETAILS structure [Windows Multimedia], msacm/ACMFORMATDETAILS, multimedia.acmformatdetails_COLLISION956, multimedia.acmformatdetails_struct'
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
req.typenames: ACMFORMATDETAILS, *PACMFORMATDETAILS, *LPACMFORMATDETAILS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tACMFORMATDETAILS
 - msacm/tACMFORMATDETAILS
 - PACMFORMATDETAILS
 - msacm/PACMFORMATDETAILS
 - ACMFORMATDETAILS
 - msacm/ACMFORMATDETAILS
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
 - ACMFORMATDETAILS
---

# ACMFORMATDETAILS structure


## -description

The <b>ACMFORMATDETAILS</b> structure details a waveform-audio format for a specific format tag for an ACM driver.

## -struct-fields

### -field cbStruct

Size, in bytes, of the <b>ACMFORMATDETAILS</b> structure. This member must be initialized before an application calls the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a> or <a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a> function. The size specified by this member must be large enough to contain the base <b>ACMFORMATDETAILS</b> structure. When the <b>acmFormatDetails</b> function returns, this member contains the actual size of the information returned. The returned information will never exceed the requested size.

### -field dwFormatIndex

Index of the format to retrieve details for. The index ranges from zero to one less than the number of standard formats supported by an ACM driver for a format tag. The number of standard formats supported by a driver for a format tag is contained in the [ACMFORMATTAGDETAILS](./nf-msacm-acmformattagdetails.md) structure. The <b>dwFormatIndex</b> member is used only when an application queries standard format details about a driver by index; otherwise, this member should be zero. Also, this member will be set to zero by the ACM when an application queries for details on a format; in other words, this member is used only for input and is never returned by the ACM or an ACM driver.

### -field dwFormatTag

Waveform-audio format tag that the <b>ACMFORMATDETAILS</b> structure describes. This member is used for input for the ACM_FORMATDETAILSF_INDEX query flag. For the ACM_FORMATDETAILSF_FORMAT query flag, this member must be initialized to the same format tag as the <b>pwfx</b> member specifies. If a call to the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a> function is successful, this member is always returned. This member should be set to WAVE_FORMAT_UNKNOWN for all other query flags.

### -field fdwSupport

Driver-support flags specific to the specified format. These flags are identical to the [ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure. This member can be a combination of the following values and indicates which operations the driver supports for the format tag:

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
Driver supports conversion between two different format tags for the specified format. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM with the specified format, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CONVERTER"></a><a id="acmdriverdetails_supportf_converter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different formats of the same format tag while using the specified format. For example, if a driver supports resampling of WAVE_FORMAT_PCM to the specified format, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_FILTER"></a><a id="acmdriverdetails_supportf_filter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports a filter (which modifies data without changing any format attributes) with the specified format. For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_HARDWARE"></a><a id="acmdriverdetails_supportf_hardware"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
Driver supports hardware input and/or output of the specified format through a waveform-audio device. An application should use <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.

</td>
</tr>
</table>

### -field pwfx

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that will receive the format details. This structure requires no initialization by the application unless the ACM_FORMATDETAILSF_FORMAT flag is specified in the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a> function. In this case, the <b>wFormatTag</b> member of the <b>WAVEFORMATEX</b> structure must be equal to the <b>dwFormatTag</b> of the <b>ACMFORMATDETAILS</b> structure.

### -field cbwfx

Size, in bytes, available for <b>pwfx</b> to receive the format details. The <a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a> and <a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a> functions can be used to determine the maximum size required for any format available for the specified driver (or for all installed ACM drivers).

### -field szFormat

String that describes the format for the <b>dwFormatTag</b> type. If the <a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a> function is successful, this string is always returned.

## -see-also

[ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md)



[ACMFORMATTAGDETAILS](./nf-msacm-acmformattagdetails.md)



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>



<a href="/windows/desktop/Multimedia/audio-compression-structures">Audio Compression Structures</a>



<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformatdetails">acmFormatDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformatenum">acmFormatEnum</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmformattagdetails">acmFormatTagDetails</a>



<a href="/windows/desktop/api/msacm/nf-msacm-acmmetrics">acmMetrics</a>