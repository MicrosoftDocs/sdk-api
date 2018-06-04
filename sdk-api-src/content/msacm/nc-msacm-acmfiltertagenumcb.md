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

# ACMFILTERTAGENUMCB callback function


## -description



The <b>acmFilterTagEnumCallback</b> function specifies a callback function used with the <a href="https://msdn.microsoft.com/eaec57c2-51b8-4842-ba78-f5726c2dc31d">acmFilterTagEnum</a> function. The <b>acmFilterTagEnumCallback</b> function name is a placeholder for an application-defined function name.




## -parameters




### -param hadid

Handle to the ACM driver identifier.


### -param paftd

Pointer to an <a href="https://msdn.microsoft.com/94b31090-74ed-42ac-b904-0a90f055e03a">ACMFILTERTAGDETAILS</a> structure that contains the enumerated filter tag details.


### -param dwInstance

Application-defined value specified in <a href="https://msdn.microsoft.com/eaec57c2-51b8-4842-ba78-f5726c2dc31d">acmFilterTagEnum</a>.


### -param fdwSupport

Driver-support flags specific to the driver identifier <i>hadid</i>. These flags are identical to the <i>fdwSupport</i> flags of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure. This parameter can be a combination of the following values and identifies which operations the driver supports with the filter tag.

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
<td><b>ACMDRIVERDETAILS_SUPPORTF_ASYNC</b></td>
<td>Driver supports asynchronous conversions with the specified filter tag.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_CODEC</b></td>
<td>Driver supports conversion between two different format tags while using the specified filter tag. For example, if a driver supports compression from <b>WAVE_FORMAT_PCM</b> to <b>WAVE_FORMAT_ADPCM</b> with the specified filter tag, this flag is set.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></td>
<td>Driver supports conversion between two different formats of the same format tag while using the specified filter tag. For example, if a driver supports resampling of <b>WAVE_FORMAT_PCM</b> with the specified filter tag, this flag is set.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on <b>WAVE_FORMAT_PCM</b>, this flag is set.</td>
</tr>
<tr>
<td><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></td>
<td>Driver supports hardware input, output, or both with the specified filter tag through a waveform-audio device. An application should use the <a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a> function with the <b>ACM_METRIC_HARDWARE_WAVE_INPUT</b> and <b>ACM_METRIC_HARDWARE_WAVE_OUTPUT</b> metric indices to get the waveform-audio device identifiers associated with the supporting ACM driver.</td>
</tr>
</table>
 


## -returns



The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.




## -remarks



The <a href="https://msdn.microsoft.com/eaec57c2-51b8-4842-ba78-f5726c2dc31d">acmFilterTagEnum</a> function returns <b>MMSYSERR_NOERROR</b> (zero) if no filter tags are to be enumerated. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="https://msdn.microsoft.com/f037cab8-a1f4-487f-ab0a-11e11993b007">acmDriverAdd</a>, <a href="https://msdn.microsoft.com/7182d452-a935-4ed5-808a-595fca4f0429">acmDriverRemove</a>, and <a href="https://msdn.microsoft.com/62ab009e-b8fe-4b92-ba0f-a98cd761307b">acmDriverPriority</a>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

