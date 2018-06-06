---
UID: NC:msacm.ACMFORMATTAGENUMCB
title: ACMFORMATTAGENUMCB
author: windows-sdk-content
description: The acmFormatTagEnumCallback function specifies a callback function used with the acmFormatTagEnum function. The acmFormatTagEnumCallback name is a placeholder for an application-defined function name.
old-location: multimedia\acmformattagenumcallback.htm
old-project: Multimedia
ms.assetid: 4ab42348-0fd2-418f-a2e6-db478d3a3e33
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ACMFORMATTAGENUMCB, ACMFORMATTAGENUMCB callback, ACMFORMATTAGENUMCB callback function [Windows Multimedia], ACMFORMATTAGENUMCBA, ACMFORMATTAGENUMCBW, _win32_acmFormatTagEnumCallback, acmFormatTagEnumCallback, msacm/ACMFORMATTAGENUMCB, msacm/ACMFORMATTAGENUMCBA, msacm/ACMFORMATTAGENUMCBW, multimedia.acmformattagenumcallback
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
tech.root: 
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - ACMFORMATTAGENUMCB
 - ACMFORMATTAGENUMCBA
 - ACMFORMATTAGENUMCBW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ACMFORMATTAGENUMCB callback function


## -description



The <b>acmFormatTagEnumCallback</b> function specifies a callback function used with the <a href="https://msdn.microsoft.com/1693a7ee-1d9b-494e-8d28-b5e9279951e1">acmFormatTagEnum</a> function. The <b>acmFormatTagEnumCallback</b> name is a placeholder for an application-defined function name.




## -parameters




### -param hadid

Handle to the ACM driver identifier.


### -param paftd

Pointer to an <a href="https://msdn.microsoft.com/134cccb1-4065-407f-a02b-7bd340b4a8cf">ACMFORMATTAGDETAILS</a> structure that contains the enumerated format tag details.


### -param dwInstance

Application-defined value specified in the <a href="https://msdn.microsoft.com/1693a7ee-1d9b-494e-8d28-b5e9279951e1">acmFormatTagEnum</a> function.


### -param fdwSupport

Driver-support flags specific to the format tag. These flags are identical to the <b>fdwSupport</b> flags of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure. This parameter can be a combination of the following values and indicates which operations the driver supports with the format tag.

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
<td>ACMDRIVERDETAILS_SUPPORTF_ASYNC</td>
<td>Driver supports asynchronous conversions with the specified filter tag.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CODEC</td>
<td>Driver supports conversion between two different format tags where one of the tags is the specified format tag. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</td>
<td>Driver supports conversion between two different formats of the specified format tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_FILTER</td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on the specified format tag, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</td>
<td>Driver supports hardware input, output, or both of the specified format tag through a waveform-audio device. An application should use <a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a> with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.</td>
</tr>
</table>
 


## -returns



The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.




## -remarks



The <a href="https://msdn.microsoft.com/1693a7ee-1d9b-494e-8d28-b5e9279951e1">acmFormatTagEnum</a> function will return MMSYSERR_NOERROR (zero) if no format tags are to be enumerated. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="https://msdn.microsoft.com/f037cab8-a1f4-487f-ab0a-11e11993b007">acmDriverAdd</a>, <a href="https://msdn.microsoft.com/7182d452-a935-4ed5-808a-595fca4f0429">acmDriverRemove</a>, and <a href="https://msdn.microsoft.com/62ab009e-b8fe-4b92-ba0f-a98cd761307b">acmDriverPriority</a>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

