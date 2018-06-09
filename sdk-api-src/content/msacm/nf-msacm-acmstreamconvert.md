---
UID: NF:msacm.acmStreamConvert
title: acmStreamConvert function
author: windows-sdk-content
description: The acmStreamConvert function requests the ACM to perform a conversion on the specified conversion stream. A conversion may be synchronous or asynchronous, depending on how the stream was opened.
old-location: multimedia\acmstreamconvert.htm
old-project: Multimedia
ms.assetid: 97537dcc-acf4-4fea-b17f-2301a72a6a78
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "_win32_acmStreamConvert, acmStreamConvert, acmStreamConvert function [Windows Multimedia], msacm/acmStreamConvert, multimedia.acmstreamconvert"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmStreamConvert
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmStreamConvert function


## -description



The <b>acmStreamConvert</b> function requests the ACM to perform a conversion on the specified conversion stream. A conversion may be synchronous or asynchronous, depending on how the stream was opened.




## -parameters




### -param has

Handle to the open conversion stream.


### -param pash

Pointer to a stream header that describes source and destination buffers for a conversion. This header must have been prepared previously by using the <a href="https://msdn.microsoft.com/ab90ac5f-6f39-4d26-96fc-5258d4e353cd">acmStreamPrepareHeader</a> function.


### -param fdwConvert

Flags for doing the conversion. The following values are defined.

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
<td>ACM_STREAMCONVERTF_BLOCKALIGN</td>
<td>Only integral numbers of blocks will be converted. Converted data will end on block-aligned boundaries. An application should use this flag for all conversions on a stream until there is not enough source data to convert to a block-aligned destination. In this case, the last conversion should be specified without this flag.</td>
</tr>
<tr>
<td>ACM_STREAMCONVERTF_END</td>
<td>ACM conversion stream should begin returning pending instance data. For example, if a conversion stream holds instance data, such as the end of an echo filter operation, this flag will cause the stream to start returning this remaining data with optional source data. This flag can be specified with the ACM_STREAMCONVERTF_START flag.</td>
</tr>
<tr>
<td>ACM_STREAMCONVERTF_START</td>
<td>ACM conversion stream should reinitialize its instance data. For example, if a conversion stream holds instance data, such as delta or predictor information, this flag will restore the stream to starting defaults. This flag can be specified with the ACM_STREAMCONVERTF_END flag.</td>
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
<dt><b>ACMERR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The stream header specified in <i>pash</i> is currently in use and cannot be reused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ACMERR_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The stream header specified in <i>pash</i> is currently not prepared by the <a href="https://msdn.microsoft.com/ab90ac5f-6f39-4d26-96fc-5258d4e353cd">acmStreamPrepareHeader</a> function.

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
 




## -remarks



You must use the <a href="https://msdn.microsoft.com/ab90ac5f-6f39-4d26-96fc-5258d4e353cd">acmStreamPrepareHeader</a> function to prepare the source and destination buffers before they are passed to <b>acmStreamConvert</b>.

If an asynchronous conversion request is successfully queued by the ACM or driver and the conversion is later determined to be impossible, the <a href="https://msdn.microsoft.com/723e96d8-f098-4e08-862a-a9fea8d2fbe3">ACMSTREAMHEADER</a> structure is posted back to the application's callback function with the <b>cbDstLengthUsed</b> member set to zero.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

