---
UID: NF:msacm.acmFormatTagDetails
title: acmFormatTagDetails function
author: windows-sdk-content
description: The acmFormatTagDetails function queries the ACM for details on a specific waveform-audio format tag.
old-location: multimedia\acmformattagdetails.htm
tech.root: Multimedia
ms.assetid: 294d9e8b-de47-4ebe-8989-558469ba1356
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "_win32_acmFormatTagDetails, acmFormatTagDetails, acmFormatTagDetails function [Windows Multimedia], acmFormatTagDetailsA, acmFormatTagDetailsW, msacm/acmFormatTagDetails, msacm/acmFormatTagDetailsA, msacm/acmFormatTagDetailsW, multimedia.acmformattagdetails"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- acmFormatTagDetails
: 
---

# acmFormatTagDetails function


## -description



The <b>acmFormatTagDetails</b> function queries the ACM for details on a specific waveform-audio format tag.




## -parameters




### -param had

Handle to the ACM driver to query for waveform-audio format tag details. If this parameter is <b>NULL</b>, the ACM uses the details from the first suitable ACM driver. An application must specify a valid handle or driver identifier when using the ACM_FORMATTAGDETAILSF_INDEX query type. Driver identifiers for disabled drivers are not allowed.


### -param paftd

Pointer to the <a href="https://msdn.microsoft.com/134cccb1-4065-407f-a02b-7bd340b4a8cf">ACMFORMATTAGDETAILS</a> structure that is to receive the format tag details.


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
<td>A format tag was given in the <b>dwFormatTag</b> member of the <a href="https://msdn.microsoft.com/134cccb1-4065-407f-a02b-7bd340b4a8cf">ACMFORMATTAGDETAILS</a> structure. The format tag details will be returned in the structure pointed to by <i>paftd</i>. If an application specifies an ACM driver handle for <i>had</i>, details on the format tag will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds the first acceptable driver to return the details.</td>
</tr>
<tr>
<td>ACM_FORMATTAGDETAILSF_INDEX</td>
<td>A format tag index was given in the <b>dwFormatTagIndex</b> member of the <b>ACMFORMATTAGDETAILS</b> structure. The format tag and details will be returned in the structure defined by <i>paftd</i>. The index ranges from zero to one less than the <b>cFormatTags</b> member returned in the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure for an ACM driver. An application must specify a driver handle for <i>had</i> when retrieving format tag details with this flag.</td>
</tr>
<tr>
<td>ACM_FORMATTAGDETAILSF_LARGESTSIZE</td>
<td>Details on the format tag with the largest format size, in bytes, are to be returned. The <b>dwFormatTag</b> member of the <a href="https://msdn.microsoft.com/134cccb1-4065-407f-a02b-7bd340b4a8cf">ACMFORMATTAGDETAILS</a> structure must either be WAVE_FORMAT_UNKNOWN or the format tag to find the largest size for. If an application specifies an ACM driver handle for <i>had</i>, details on the largest format tag will be returned for that driver. If an application specifies <b>NULL</b> for <i>had</i>, the ACM finds an acceptable driver with the largest format tag requested to return the details.</td>
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




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

