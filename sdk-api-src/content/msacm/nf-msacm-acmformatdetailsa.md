---
UID: NF:msacm.acmFormatDetailsA
title: acmFormatDetailsA function (msacm.h)
description: The acmFormatDetails function queries the ACM for format details for a specific waveform-audio format tag. (acmFormatDetailsA)
helpviewer_keywords: ["acmFormatDetailsA", "msacm/acmFormatDetailsA"]
old-location: multimedia\acmformatdetails.htm
tech.root: Multimedia
ms.assetid: 2a6a9b8f-758b-4443-b1c7-e277f22bac5b
ms.date: 12/05/2018
ms.keywords: _win32_acmFormatDetails, acmFormatDetails, acmFormatDetails function [Windows Multimedia], acmFormatDetailsA, acmFormatDetailsW, msacm/acmFormatDetails, msacm/acmFormatDetailsA, msacm/acmFormatDetailsW, multimedia.acmformatdetails
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFormatDetailsW (Unicode) and acmFormatDetailsA (ANSI)
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
 - acmFormatDetailsA
 - msacm/acmFormatDetailsA
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
 - acmFormatDetails
 - acmFormatDetailsA
 - acmFormatDetailsW
---

# acmFormatDetailsA function


## -description

The <b>acmFormatDetails</b> function queries the ACM for format details for a specific waveform-audio format tag.

## -parameters

### -param had

Handle to the ACM driver to query for waveform-audio format details for a format tag. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver.

### -param pafd

Pointer to an [ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure to contain the format details for the given format tag.

### -param fdwDetails

Flags for getting the waveform-audio format tag details. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_FORMATDETAILSF_FORMAT</td>
[ACMFORMATDETAILS](./nf-msacm-acmformatdetails.md) structure was given and the remaining details should be returned. The <b>dwFormatTag</b> member of the <b>ACMFORMATDETAILS</b> structure must be initialized to the same format tag as <b>pwfx</b> specifies. This query type can be used to get a string description of an arbitrary format structure. If an application specifies an ACM driver handle for <i>had</i>, details on the format will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds the first acceptable driver to return the details.</td>
</tr>
<tr>
<td>ACM_FORMATDETAILSF_INDEX</td>
<td>A format index for the format tag was given in the <b>dwFormatIndex</b> member of the <b>ACMFORMATDETAILS</b> structure. The format details will be returned in the structure defined by <i>pafd</i>. The index ranges from zero to one less than the <b>cStandardFormats</b> member returned in the <b>ACMFORMATTAGDETAILS</b> structure for a format tag. An application must specify a driver handle for <i>had</i> when retrieving format details with this flag. For information about which members should be initialized before calling this function, see the <b>ACMFORMATDETAILS</b> structure.</td>
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
> The msacm.h header defines ACMFORMATDETAILS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
