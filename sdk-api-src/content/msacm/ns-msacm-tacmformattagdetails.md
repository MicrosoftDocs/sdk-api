---
UID: NS:msacm.tACMFORMATTAGDETAILS
title: tACMFORMATTAGDETAILS
author: windows-sdk-content
description: The ACMFORMATTAGDETAILS structure details a waveform-audio format tag for an ACM driver.
old-location: multimedia\acmformattagdetails_struct.htm
tech.root: Multimedia
ms.assetid: 134cccb1-4065-407f-a02b-7bd340b4a8cf
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "*LPACMFORMATTAGDETAILS, *PACMFORMATTAGDETAILS, ACMDRIVERDETAILS_SUPPORTF_ASYNC, ACMDRIVERDETAILS_SUPPORTF_CODEC, ACMDRIVERDETAILS_SUPPORTF_CONVERTER, ACMDRIVERDETAILS_SUPPORTF_FILTER, ACMDRIVERDETAILS_SUPPORTF_HARDWARE, ACMFORMATTAGDETAILS, ACMFORMATTAGDETAILS structure [Windows Multimedia], msacm/ACMFORMATTAGDETAILS, multimedia.acmformattagdetails_COLLISION956, multimedia.acmformattagdetails_struct, tACMFORMATTAGDETAILS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - Msacm.h
api_name:
 - ACMFORMATTAGDETAILS
product: Windows
targetos: Windows
req.typenames: ACMFORMATTAGDETAILS, *PACMFORMATTAGDETAILS, *LPACMFORMATTAGDETAILS
req.redist: 
---

# tACMFORMATTAGDETAILS structure


## -description



The <b>ACMFORMATTAGDETAILS</b> structure details a waveform-audio format tag for an ACM driver.




## -struct-fields




### -field cbStruct

Size, in bytes, of the <b>ACMFORMATTAGDETAILS</b> structure. This member must be initialized before an application calls the <a href="https://msdn.microsoft.com/294d9e8b-de47-4ebe-8989-558469ba1356">acmFormatTagDetails</a> or <a href="https://msdn.microsoft.com/1693a7ee-1d9b-494e-8d28-b5e9279951e1">acmFormatTagEnum</a> function. The size specified by this member must be large enough to contain the base <b>ACMFORMATTAGDETAILS</b> structure. When the <b>acmFormatTagDetails</b> function returns, this member contains the actual size of the information returned. The returned information will never exceed the requested size.


### -field dwFormatTagIndex

Index of the format tag for which details will be retrieved. The index ranges from zero to one less than the number of format tags supported by an ACM driver. The number of format tags supported by a driver is contained in the <b>cFormatTags</b> member of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure. The <b>dwFormatTagIndex</b> member is used only when querying format tag details on a driver by index; otherwise, this member should be zero.


### -field dwFormatTag

Waveform-audio format tag that the <b>ACMFORMATTAGDETAILS</b> structure describes. This member is used for input for the ACM_FORMATTAGDETAILSF_FORMATTAG and ACM_FORMATTAGDETAILSF_LARGESTSIZE query flags. If the <a href="https://msdn.microsoft.com/294d9e8b-de47-4ebe-8989-558469ba1356">acmFormatTagDetails</a> function is successful, this member is always returned. This member should be set to WAVE_FORMAT_UNKNOWN for all other query flags.


### -field cbFormatSize

Largest total size, in bytes, of a waveform-audio format of the <b>dwFormatTag</b> type. For example, this member will be 16 for WAVE_FORMAT_PCM and 50 for WAVE_FORMAT_ADPCM.


### -field fdwSupport

Driver-support flags specific to the format tag. These flags are identical to the <b>fdwSupport</b> flags of the <a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a> structure. This member may be some combination of the following values and refer to what operations the driver supports with the format tag:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_ASYNC"></a><a id="acmdriverdetails_supportf_async"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports asynchronous conversions with the specified format tag.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CODEC"></a><a id="acmdriverdetails_supportf_codec"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CODEC</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different format tags where one of the tags is the specified format tag. For example, if a driver supports compression from WAVE_FORMAT_PCM to WAVE_FORMAT_ADPCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_CONVERTER"></a><a id="acmdriverdetails_supportf_converter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_CONVERTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports conversion between two different formats of the specified format tag. For example, if a driver supports resampling of WAVE_FORMAT_PCM, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_FILTER"></a><a id="acmdriverdetails_supportf_filter"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Driver supports a filter (modification of the data without changing any of the format attributes). For example, if a driver supports volume or echo operations on the specified format tag, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="ACMDRIVERDETAILS_SUPPORTF_HARDWARE"></a><a id="acmdriverdetails_supportf_hardware"></a><dl>
<dt><b>ACMDRIVERDETAILS_SUPPORTF_HARDWARE</b></dt>
</dl>
</td>
<td width="60%">
Driver supports hardware input, output, or both of the specified format tag through a waveform-audio device. An application should use the <a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a> function with the ACM_METRIC_HARDWARE_WAVE_INPUT and ACM_METRIC_HARDWARE_WAVE_OUTPUT metric indexes to get the waveform-audio device identifiers associated with the supporting ACM driver.

</td>
</tr>
</table>
 


### -field cStandardFormats

Number of standard formats of the <b>dwFormatTag</b> type; that is, the combination of all sample rates, bits per sample, channels, and so on. This value can specify all formats supported by the driver, but not necessarily.


### -field szFormatTag

String that describes the <b>dwFormatTag</b> type. If the <a href="https://msdn.microsoft.com/294d9e8b-de47-4ebe-8989-558469ba1356">acmFormatTagDetails</a> function is successful, this string is always returned.


## -see-also




<a href="https://msdn.microsoft.com/b45b26e2-a9c0-4d01-9989-a071d9c73993">ACMDRIVERDETAILS</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>



<a href="https://msdn.microsoft.com/19ef4569-e6fc-480a-8659-98df3d36d05f">Audio Compression Structures</a>



<a href="https://msdn.microsoft.com/294d9e8b-de47-4ebe-8989-558469ba1356">acmFormatTagDetails</a>



<a href="https://msdn.microsoft.com/1693a7ee-1d9b-494e-8d28-b5e9279951e1">acmFormatTagEnum</a>



<a href="https://msdn.microsoft.com/30b6dc13-b523-4c42-aa35-c86b3ebe04c3">acmMetrics</a>
 

 

