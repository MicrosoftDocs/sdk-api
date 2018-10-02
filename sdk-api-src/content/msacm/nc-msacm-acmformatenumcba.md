---
UID: NC:msacm.ACMFORMATENUMCBA
title: ACMFORMATENUMCBA
author: windows-sdk-content
description: The acmFormatEnumCallback function specifies a callback function used with the acmFormatEnum function. The acmFormatEnumCallback name is a placeholder for the application-defined function name.
old-location: multimedia\acmformatenumcallback.htm
tech.root: Multimedia
ms.assetid: 58775258-c42c-4d59-8922-c478b5bdf0d7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ACMFORMATENUMCB, ACMFORMATENUMCB callback, ACMFORMATENUMCB callback function [Windows Multimedia], ACMFORMATENUMCBA, ACMFORMATENUMCBW, _win32_acmFormatEnumCallback, acmFormatEnumCallback, msacm/ACMFORMATENUMCB, msacm/ACMFORMATENUMCBA, msacm/ACMFORMATENUMCBW, multimedia.acmformatenumcallback
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
 - ACMFORMATENUMCB
 - ACMFORMATENUMCBA
 - ACMFORMATENUMCBW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ACMFORMATENUMCBA callback function


## -description



The <b>acmFormatEnumCallback</b> function specifies a callback function used with the <a href="https://msdn.microsoft.com/31da0e86-a298-4ef6-a515-4954aa120656">acmFormatEnum</a> function. The <b>acmFormatEnumCallback</b> name is a placeholder for the application-defined function name.




## -parameters




### -param hadid

Handle to the ACM driver identifier.


### -param pafd

Pointer to an <a href="https://msdn.microsoft.com/a0760541-c083-447d-a812-dd7f05afb622">ACMFORMATDETAILS</a> structure that contains the enumerated format details for a format tag.


### -param dwInstance

Application-defined value specified in the <a href="https://msdn.microsoft.com/31da0e86-a298-4ef6-a515-4954aa120656">acmFormatEnum</a> function.


### -param fdwSupport

Driver support flags specific to the driver identified by <i>hadid</i> for the specified format. These flags are identical to the <b>fdwSupport</b> flags of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure, but they are specific to the format that is being enumerated. This parameter can be a combination of the following values and indicates which operations the driver supports for the format tag.

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
<td>Driver supports conversion between two different format tags for the specified format. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM with the specified format, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</td>
<td>Driver supports conversion between two different formats of the same format tag while using the specified format. For example, if a driver supports resampling of WAVE_FORMAT_PCM to the specified format, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_FILTER</td>
<td>Driver supports a filter (modification of the data without changing any of the format attributes) with the specified format. For example, if a driver supports volume or echo operations on WAVE_FORMAT_PCM, this flag is set.</td>
</tr>
<tr>
<td>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</td>
<td>Driver supports hardware input, output, or both of the specified format tags through a waveform-audio device. An application should use the <a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.</td>
</tr>
</table>
 


## -returns



The callback function must return <b>TRUE</b> to continue enumeration or <b>FALSE</b> to stop enumeration.




## -remarks



The <a href="https://msdn.microsoft.com/31da0e86-a298-4ef6-a515-4954aa120656">acmFormatEnum</a> function will return MMSYSERR_NOERROR (zero) if no formats are to be enumerated. Moreover, the callback function will not be called.

The following functions should not be called from within the callback function: <a href="https://msdn.microsoft.com/f037cab8-a1f4-487f-ab0a-11e11993b007">acmDriverAdd</a>, <a href="https://msdn.microsoft.com/7182d452-a935-4ed5-808a-595fca4f0429">acmDriverRemove</a>, and <a href="https://msdn.microsoft.com/62ab009e-b8fe-4b92-ba0f-a98cd761307b">acmDriverPriority</a>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

