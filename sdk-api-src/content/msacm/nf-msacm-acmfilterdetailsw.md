---
UID: NF:msacm.acmFilterDetailsW
title: acmFilterDetailsW function (msacm.h)
description: The acmFilterDetails (Unicode) function queries the ACM for details about a filter with a specific waveform-audio filter tag. (acmFilterDetailsW)
helpviewer_keywords: ["_win32_acmFilterDetails", "acmFilterDetails", "acmFilterDetails function [Windows Multimedia]", "acmFilterDetailsW", "msacm/acmFilterDetails", "msacm/acmFilterDetailsW", "multimedia.acmfilterdetails"]
old-location: multimedia\acmfilterdetails.htm
tech.root: Multimedia
ms.assetid: ab29362e-fa85-4833-a2c8-df5cfacc6140
ms.date: 08/02/2022
ms.keywords: _win32_acmFilterDetails, acmFilterDetails, acmFilterDetails function [Windows Multimedia], acmFilterDetailsA, acmFilterDetailsW, msacm/acmFilterDetails, msacm/acmFilterDetailsA, msacm/acmFilterDetailsW, multimedia.acmfilterdetails
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFilterDetailsW (Unicode) and acmFilterDetailsA (ANSI)
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
 - acmFilterDetailsW
 - msacm/acmFilterDetailsW
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
 - acmFilterDetails
 - acmFilterDetailsA
 - acmFilterDetailsW
---

# acmFilterDetailsW function


## -description

The <b>acmFilterDetails</b> function queries the ACM for details about a filter with a specific waveform-audio filter tag.

## -parameters

### -param had

Handle to the ACM driver to query for waveform-audio filter details for a filter tag. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver.

### -param pafd

Pointer to the [ACMFILTERDETAILS](./nf-msacm-acmfilterdetails.md) structure that is to receive the filter details for the given filter tag.

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
<td>ACM_FILTERDETAILSF_FILTER</td>
[ACMFILTERDETAILS](./nf-msacm-acmfilterdetails.md) structure was given and the remaining details should be returned. The <b>dwFilterTag</b> member of the <b>ACMFILTERDETAILS</b> structure must be initialized to the same filter tag <b>pwfltr</b> specifies. This query type can be used to get a string description of an arbitrary filter structure. If an application specifies an ACM driver handle for <i>had</i>, details on the filter will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds the first acceptable driver to return the details.</td>
</tr>
<tr>
<td>ACM_FILTERDETAILSF_INDEX</td>
<td>A filter index for the filter tag was given in the <b>dwFilterIndex</b> member of the <b>ACMFILTERDETAILS</b> structure. The filter details will be returned in the structure defined by <i>pafd</i>. The index ranges from zero to one less than the <b>cStandardFilters</b> member returned in the <b>ACMFILTERTAGDETAILS</b> structure for a filter tag. An application must specify a driver handle for <i>had</i> when retrieving filter details with this flag. For information about what members should be initialized before calling this function, see the <b>ACMFILTERDETAILS</b> structure.</td>
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
> The msacm.h header defines ACMFILTERDETAILS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
