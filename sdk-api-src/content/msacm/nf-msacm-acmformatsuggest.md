---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# acmFormatSuggest function


## -description



The <b>acmFormatSuggest</b> function queries the ACM or a specified ACM driver to suggest a destination format for the supplied source format. For example, an application can use this function to determine one or more valid PCM formats to which a compressed format can be decompressed.




## -parameters




### -param had

Handle to an open instance of a driver to query for a suggested destination format. If this parameter is <b>NULL</b>, the ACM attempts to find the best driver to suggest a destination format.


### -param pwfxSrc

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that identifies the source format for which a destination format will be suggested by the ACM or specified driver.


### -param pwfxDst

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that will receive the suggested destination format for the <i>pwfxSrc</i> format. Depending on the <i>fdwSuggest</i> parameter, some members of the structure pointed to by <i>pwfxDst</i> may require initialization.


### -param cbwfxDst

Size, in bytes, available for the destination format. The <a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a> and <a href="https://msdn.microsoft.com/294d9e8b-de47-4ebe-8989-558469ba1356">acmFormatTagDetails</a> functions can be used to determine the maximum size required for any format available for the specified driver (or for all installed ACM drivers).


### -param fdwSuggest

Flags for matching the desired destination format. The following values are defined.

<table>
<tr>
<th>
Value
</th>
<th>
Meaning
</th>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_NCHANNELS</td>
<td>The <b>nChannels</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>nChannels</b> or fail.</td>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_NSAMPLESPERSEC</td>
<td>The <b>nSamplesPerSec</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>nSamplesPerSec</b> or fail.</td>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_WBITSPERSAMPLE</td>
<td>The <b>wBitsPerSample</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>wBitsPerSample</b> or fail.</td>
</tr>
<tr>
<td>ACM_FORMATSUGGESTF_WFORMATTAG</td>
<td>The <b>wFormatTag</b> member of the structure pointed to by <i>pwfxDst</i> is valid. The ACM will query acceptable installed drivers that can suggest a destination format matching <b>wFormatTag</b> or fail.</td>
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
 

 

