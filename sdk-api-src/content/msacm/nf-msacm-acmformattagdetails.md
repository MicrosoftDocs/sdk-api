---
UID: NF:msacm.acmFormatTagDetails
title: acmFormatTagDetails function (msacm.h)
description: The acmFormatTagDetails function queries the ACM for details on a specific waveform-audio format tag.
helpviewer_keywords: ["_win32_acmFormatTagDetails","acmFormatTagDetails","acmFormatTagDetails function [Windows Multimedia]","acmFormatTagDetailsA","acmFormatTagDetailsW","msacm/acmFormatTagDetails","msacm/acmFormatTagDetailsA","msacm/acmFormatTagDetailsW","multimedia.acmformattagdetails"]
old-location: multimedia\acmformattagdetails.htm
tech.root: Multimedia
ms.assetid: 294d9e8b-de47-4ebe-8989-558469ba1356
ms.date: 12/05/2018
ms.keywords: _win32_acmFormatTagDetails, acmFormatTagDetails, acmFormatTagDetails function [Windows Multimedia], acmFormatTagDetailsA, acmFormatTagDetailsW, msacm/acmFormatTagDetails, msacm/acmFormatTagDetailsA, msacm/acmFormatTagDetailsW, multimedia.acmformattagdetails
f1_keywords:
- msacm/acmFormatTagDetails
dev_langs:
- c++
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: acmFormatTagDetailsW (Unicode) and acmFormatTagDetailsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Msacm32.dll
- Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
- acmFormatTagDetails
- acmFormatTagDetailsA
- acmFormatTagDetailsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# acmFormatTagDetails function


## -description



The <b>acmFormatTagDetails</b> function queries the ACM for details on a specific waveform-audio format tag.




## -parameters




### -param had

Handle to the ACM driver to query for waveform-audio format tag details. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver. An application must specify a valid handle or driver identifier when using the ACM_FORMATTAGDETAILSF_INDEX query type. Driver identifiers for disabled drivers are not allowed.


### -param paftd

Pointer to the [ACMFORMATTAGDETAILS](/windows/win32/api/msacm/nf-msacm-acmformattagdetails) structure that is to receive the format tag details.


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
<td>ACM_FORMATTAGDETAILSF_FORMATTAG</td>
[ACMFORMATTAGDETAILS](/windows/win32/api/msacm/nf-msacm-acmformattagdetails) structure. The format tag details will be returned in the structure pointed to by <i>paftd</i>. If an application specifies an ACM driver handle for <i>had</i>, details on the format tag will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds the first acceptable driver to return the details.</td>
</tr>
<tr>
<td>ACM_FORMATTAGDETAILSF_INDEX</td>
[ACMDRIVERDETAILS](/windows/win32/api/msacm/nf-msacm-acmdriverdetails) structure for an ACM driver. An application must specify a driver handle for <i>had</i> when retrieving format tag details with this flag.</td>
</tr>
<tr>
<td>ACM_FORMATTAGDETAILSF_LARGESTSIZE</td>
[ACMFORMATTAGDETAILS](/windows/win32/api/msacm/nf-msacm-acmformattagdetails) structure must either be WAVE_FORMAT_UNKNOWN or the format tag to find the largest size for. If an application specifies an ACM driver handle for <i>had</i>, details on the largest format tag will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds an acceptable driver with the largest format tag requested to return the details.</td>
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




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
 

 

