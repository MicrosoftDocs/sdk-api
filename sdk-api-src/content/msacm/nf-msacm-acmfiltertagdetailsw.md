---
UID: NF:msacm.acmFilterTagDetailsW
title: acmFilterTagDetailsW function (msacm.h)
description: The acmFilterTagDetails (Unicode) function queries the ACM for details about a specific waveform-audio filter tag. (acmFilterTagDetailsW)
helpviewer_keywords: ["_win32_acmFilterTagDetails", "acmFilterTagDetails", "acmFilterTagDetails function [Windows Multimedia]", "acmFilterTagDetailsW", "msacm/acmFilterTagDetails", "msacm/acmFilterTagDetailsW", "multimedia.acmfiltertagdetails"]
old-location: multimedia\acmfiltertagdetails.htm
tech.root: Multimedia
ms.assetid: 6b1fd113-5753-4a45-974c-ecf3f5d27866
ms.date: 08/02/2022
ms.keywords: _win32_acmFilterTagDetails, acmFilterTagDetails, acmFilterTagDetails function [Windows Multimedia], acmFilterTagDetailsA, acmFilterTagDetailsW, msacm/acmFilterTagDetails, msacm/acmFilterTagDetailsA, msacm/acmFilterTagDetailsW, multimedia.acmfiltertagdetails
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFilterTagDetailsW (Unicode) and acmFilterTagDetailsA (ANSI)
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
 - acmFilterTagDetailsW
 - msacm/acmFilterTagDetailsW
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
 - acmFilterTagDetails
 - acmFilterTagDetailsA
 - acmFilterTagDetailsW
---

# acmFilterTagDetailsW function


## -description

The <b>acmFilterTagDetails</b> function queries the ACM for details about a specific waveform-audio filter tag.

## -parameters

### -param had

Handle to the ACM driver to query for waveform-audio filter tag details. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver. An application must specify a valid <b>HACMDRIVER</b> or <b>HACMDRIVERID</b> identifier when using the ACM_FILTERTAGDETAILSF_INDEX query type. Driver identifiers for disabled drivers are not allowed.

### -param paftd

Pointer to the [ACMFILTERTAGDETAILS](./nf-msacm-acmfiltertagdetails.md) structure that is to receive the filter tag details.

### -param fdwDetails

Flags for getting the details. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_FILTERTAGDETAILSF_FILTERTAG</td>
[ACMFILTERTAGDETAILS](./nf-msacm-acmfiltertagdetails.md) structure. The filter tag details will be returned in the structure pointed to by <i>paftd</i>. If an application specifies an ACM driver handle for <i>had</i>, details on the filter tag will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds the first acceptable driver to return the details.</td>
</tr>
<tr>
<td>ACM_FILTERTAGDETAILSF_INDEX</td>
[ACMDRIVERDETAILS](./nf-msacm-acmdriverdetails.md) structure for an ACM driver. An application must specify a driver handle for <i>had</i> when retrieving filter tag details with this flag.</td>
</tr>
<tr>
<td>ACM_FILTERTAGDETAILSF_LARGESTSIZE</td>
<td>Details on the filter tag with the largest filter size, in bytes, are to be returned. The <b>dwFilterTag</b> member must either be WAVE_FILTER_UNKNOWN or the filter tag to find the largest size for. If an application specifies an ACM driver handle for <i>had</i>, details on the largest filter tag will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds an acceptable driver with the largest filter tag requested to return the details.</td>
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
<dt><b>ACMERR_NOTPOSSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The details requested are not available.

</td>
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

## -remarks

> [!NOTE]
> The msacm.h header defines ACMFILTERTAGDETAILS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
