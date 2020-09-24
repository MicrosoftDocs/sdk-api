---
UID: NF:msacm.acmStreamOpen
title: acmStreamOpen function (msacm.h)
description: The acmStreamOpen function opens an ACM conversion stream. Conversion streams are used to convert data from one specified audio format to another.
helpviewer_keywords: ["_win32_acmStreamOpen","acmStreamOpen","acmStreamOpen function [Windows Multimedia]","msacm/acmStreamOpen","multimedia.acmstreamopen"]
old-location: multimedia\acmstreamopen.htm
tech.root: Multimedia
ms.assetid: 9e323d35-e640-4c6d-ab74-c4abacaea1bd
ms.date: 12/05/2018
ms.keywords: _win32_acmStreamOpen, acmStreamOpen, acmStreamOpen function [Windows Multimedia], msacm/acmStreamOpen, multimedia.acmstreamopen
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmStreamOpen
 - msacm/acmStreamOpen
dev_langs:
 - c++
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

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that identifies the desired source format for the conversion.

### -param pwfxDst

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that identifies the desired destination format for the conversion.

### -param pwfltr

Pointer to a [WAVEFILTER](../mmreg/ns-mmreg-wavefilter.md) structure that identifies the desired filtering operation to perform on the conversion stream. If no filtering operation is desired, this parameter can be <b>NULL</b>. If a filter is specified, the source (<i>pwfxSrc</i>) and destination (<i>pwfxDst</i>) formats must be the same.

### -param dwCallback

Pointer to a callback function, a handle of a window, or a handle of an event. A callback function will be called only if the conversion stream is opened with the ACM_STREAMOPENF_ASYNC flag. A callback function is notified when the conversion stream is opened or closed and after each buffer is converted. If the conversion stream is opened without the ACM_STREAMOPENF_ASYNC flag, this parameter should be set to zero.

### -param dwInstance

User-instance data passed to the callback function specified by the <i>dwCallback</i> parameter. This parameter is not used with window and event callbacks. If the conversion stream is opened without the ACM_STREAMOPENF_ASYNC flag, this parameter should be set to zero.

### -param fdwOpen

Flags for opening the conversion stream. The following values are defined.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>ACM_STREAMOPENF_ASYNC</td>
[ACMSTREAMHEADER](./ns-msacm-acmstreamheader.md) structure for the ACMSTREAMHEADER_STATUSF_DONE flag.</td>
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
<td>The <i>dwCallback</i> parameter is a callback procedure address. The function prototype must conform to the <a href="/previous-versions/dd742925(v=vs.85)">acmStreamConvertCallback</a> prototype.</td>
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

If an application uses a window to receive callback information, the MM_ACM_OPEN, MM_ACM_CLOSE, and MM_ACM_DONE messages are sent to the window procedure function to indicate the progress of the conversion stream. In this case, the [ACMSTREAMHEADER](./ns-msacm-acmstreamheader.md) structure for MM_ACM_DONE, but it is not used for MM_ACM_OPEN and MM_ACM_CLOSE.

If an application uses a function to receive callback information, the MM_ACM_OPEN, MM_ACM_CLOSE, and MM_ACM_DONE messages are sent to the function to indicate the progress of waveform-audio output. The callback function must reside in a dynamic-link library (DLL).

If an application uses an event for callback notification, the event is signaled to indicate the progress of the conversion stream. The event will be signaled when a stream is opened, after each buffer is converted, and when the stream is closed.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>