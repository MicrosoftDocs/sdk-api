---
UID: NC:msacm.ACMFILTERENUMCBW
title: ACMFILTERENUMCBW
author: windows-sdk-content
description: The acmFilterEnumCallback function specifies a callback function used with the acmFilterEnum function. The acmFilterEnumCallback name is a placeholder for an application-defined function name.
old-location: multimedia\acmfilterenumcallback.htm
tech.root: Multimedia
ms.assetid: 8d2eb1eb-97a3-4001-bec0-7bb9b107d38e
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ACMFILTERENUMCB, ACMFILTERENUMCB callback, ACMFILTERENUMCB callback function [Windows Multimedia], ACMFILTERENUMCBA, ACMFILTERENUMCBW, _win32_acmFilterEnumCallback, acmFilterEnumCallback, msacm/ACMFILTERENUMCB, msacm/ACMFILTERENUMCBA, msacm/ACMFILTERENUMCBW, multimedia.acmfilterenumcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - ACMFILTERENUMCB
 - ACMFILTERENUMCBA
 - ACMFILTERENUMCBW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ACMFILTERENUMCBW callback function


## -description



The <b>acmFilterEnumCallback</b> function specifies a callback function used with the <a href="https://msdn.microsoft.com/ee8154d6-3aa1-49ce-96c5-7b8526f02a8a">acmFilterEnum</a> function. The <b>acmFilterEnumCallback</b> name is a placeholder for an application-defined function name.




## -parameters




### -param hadid

Handle to the ACM driver identifier.


### -param pafd

Pointer to an <a href="https://msdn.microsoft.com/c0423701-b957-4f77-a565-f6f761614389">ACMFILTERDETAILS</a> structure that contains the enumerated filter details for a filter tag.


### -param dwInstance

Application-defined value specified in <a href="https://msdn.microsoft.com/ee8154d6-3aa1-49ce-96c5-7b8526f02a8a">acmFilterEnum</a>.


### -param fdwSupport

Driver-support flags specific to the driver identified by <i>hadid</i> for the specified filter. These flags are identical to the <b>fdwSupport</b> flags of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure, but they are specific to the filter that is being enumerated. This parameter can be a combination of the following values and identifies which operations the driver supports for the filter tag.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_ASYNC</td>
<td>Driver supports asynchronous conversions with the specified filter tag.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CODEC</td>
<td>Driver supports conversion between two different format tags while using the specified filter. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM with the specified filter, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</td>
<td>Driver supports conversion between two different formats of the same format tag while using the specified filter. For example, if a driver supports resampling of WAVE_FORMAT_PCM with the specified filter, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_FILTER</td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</td>
<td>Driver supports hardware input, output, or both with the specified filter through a waveform-audio device. An application should use the <a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indices to get the waveform-audio device identifiers associated with the supporting ACM driver.</td>
</tr>
</table>
 


## -returns



The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.




## -remarks



The <b>acmFilterEnum</b> function will return MMSYSERR_NOERROR (zero) if no filters are to be enumerated. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <b>acmDriverAdd</b>, <b>acmDriverRemove</b>, and <b>acmDriverPriority</b>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

