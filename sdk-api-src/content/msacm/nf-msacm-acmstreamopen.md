---
UID: NF:msacm.acmStreamOpen
title: acmStreamOpen function
author: windows-sdk-content
description: The acmStreamOpen function opens an ACM conversion stream. Conversion streams are used to convert data from one specified audio format to another.
old-location: multimedia\acmstreamopen.htm
old-project: Multimedia
ms.assetid: 9e323d35-e640-4c6d-ab74-c4abacaea1bd
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "_win32_acmStreamOpen, acmStreamOpen, acmStreamOpen function [Windows Multimedia], msacm/acmStreamOpen, multimedia.acmstreamopen"
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
 - acmStreamOpen
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmStreamOpen function


## -description



The <b>acmStreamOpen</b> function opens an ACM conversion stream. Conversion streams are used to convert data from one specified audio format to another.




## -parameters




### -param phas

Pointer to a handle that will receive the new stream handle that can be used to perform conversions. This handle is used to identify the stream in calls to other ACM stream conversion functions. If the ACM_STREAMOPENF_QUERY flag is specified, this parameter should be <b>NULL</b>.


### -param had

Handle to an ACM driver. If this handle is specified, it identifies a specific driver to be used for a conversion stream. If this parameter is <b>NULL</b>, all suitable installed ACM drivers are queried until a match is found.


### -param pwfxSrc

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that identifies the desired source format for the conversion.


### -param pwfxDst

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that identifies the desired destination format for the conversion.


### -param pwfltr

Pointer to a <a href="https://msdn.microsoft.com/dea3df47-88a2-439f-bf07-b5c592bf23e8">WAVEFILTER</a> structure that identifies the desired filtering operation to perform on the conversion stream. If no filtering operation is desired, this parameter can be <b>NULL</b>. If a filter is specified, the source (<i>pwfxSrc</i>) and destination (<i>pwfxDst</i>) formats must be the same.


### -param dwCallback

Pointer to a callback function, a handle of a window, or a handle of an event. A callback function will be called only if the conversion stream is opened with the ACM_STREAMOPENF_ASYNC flag. A callback function is notified when the conversion stream is opened or closed and after each buffer is converted. If the conversion stream is opened without the ACM_STREAMOPENF_ASYNC flag, this parameter should be set to zero.


### -param dwInstance

User-instance data passed to the callback function specified by the <i>dwCallback</i> parameter. This parameter is not used with window and event callbacks. If the conversion stream is opened without the ACM_STREAMOPENF_ASYNC flag, this parameter should be set to zero.


### -param fdwOpen

Flags for opening the conversion stream. The following values are defined.

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
<td>ACM_STREAMOPENF_ASYNC</td>
<td>Stream conversion should be performed asynchronously. If this flag is specified, the application can use a callback function to be notified when the conversion stream is opened and closed and after each buffer is converted. In addition to using a callback function, an application can examine the <b>fdwStatus</b> member of the <a href="https://msdn.microsoft.com/723e96d8-f098-4e08-862a-a9fea8d2fbe3">ACMSTREAMHEADER</a> structure for the ACMSTREAMHEADER_STATUSF_DONE flag.</td>
</tr>
<tr>
<td>ACM_STREAMOPENF_NONREALTIME</td>
<td>ACM will not consider time constraints when converting the data. By default, the driver will attempt to convert the data in real time. For some formats, specifying this flag might improve the audio quality or other characteristics.</td>
</tr>
<tr>
<td>ACM_STREAMOPENF_QUERY</td>
<td>ACM will be queried to determine whether it supports the given conversion. A conversion stream will not be opened, and no handle will be returned in the <i>phas</i> parameter.</td>
</tr>
<tr>
<td>CALLBACK_EVENT</td>
<td>The <i>dwCallback</i> parameter is a handle of an event.</td>
</tr>
<tr>
<td>CALLBACK_FUNCTION</td>
<td>The <i>dwCallback</i> parameter is a callback procedure address. The function prototype must conform to the <a href="https://msdn.microsoft.com/5849ce87-ac63-4e0b-868e-68cd284122aa">acmStreamConvertCallback</a> prototype.</td>
</tr>
<tr>
<td>CALLBACK_WINDOW</td>
<td>The <i>dwCallback</i> parameter is a window handle.</td>
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
The requested operation cannot be performed.

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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate resources.

</td>
</tr>
</table>
 




## -remarks



If an ACM driver cannot perform real-time conversions and the ACM_STREAMOPENF_NONREALTIME flag is not specified for the <i>fdwOpen</i> parameter, the open operation will fail returning an ACMERR_NOTPOSSIBLE error code. An application can use the ACM_STREAMOPENF_QUERY flag to determine if real-time conversions are supported for input.

If an application uses a window to receive callback information, the MM_ACM_OPEN, MM_ACM_CLOSE, and MM_ACM_DONE messages are sent to the window procedure function to indicate the progress of the conversion stream. In this case, the <i>wParam</i> parameter identifies the <b>HACMSTREAM</b> handle. The <i>lParam</i> parameter identifies the <a href="https://msdn.microsoft.com/723e96d8-f098-4e08-862a-a9fea8d2fbe3">ACMSTREAMHEADER</a> structure for MM_ACM_DONE, but it is not used for MM_ACM_OPEN and MM_ACM_CLOSE.

If an application uses a function to receive callback information, the MM_ACM_OPEN, MM_ACM_CLOSE, and MM_ACM_DONE messages are sent to the function to indicate the progress of waveform-audio output. The callback function must reside in a dynamic-link library (DLL).

If an application uses an event for callback notification, the event is signaled to indicate the progress of the conversion stream. The event will be signaled when a stream is opened, after each buffer is converted, and when the stream is closed.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

