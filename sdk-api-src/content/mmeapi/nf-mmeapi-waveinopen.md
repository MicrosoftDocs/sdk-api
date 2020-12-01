---
UID: NF:mmeapi.waveInOpen
title: waveInOpen function (mmeapi.h)
description: The waveInOpen function opens the given waveform-audio input device for recording.
helpviewer_keywords: ["_win32_waveInOpen","mmeapi/waveInOpen","multimedia.waveinopen","waveInOpen","waveInOpen function [Windows Multimedia]"]
old-location: multimedia\waveinopen.htm
tech.root: Multimedia
ms.assetid: 41b5b581-d35c-48ad-adcf-659126c4af50
ms.date: 12/05/2018
ms.keywords: _win32_waveInOpen, mmeapi/waveInOpen, multimedia.waveinopen, waveInOpen, waveInOpen function [Windows Multimedia]
req.header: mmeapi.h
req.include-header: Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - waveInOpen
 - mmeapi/waveInOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - waveInOpen
---

# waveInOpen function


## -description

The <b>waveInOpen</b> function opens the given waveform-audio input device for recording.

## -parameters

### -param phwi

Pointer to a buffer that receives a handle identifying the open waveform-audio input device. Use this handle to identify the device when calling other waveform-audio input functions. This parameter can be <b>NULL</b> if <b>WAVE_FORMAT_QUERY</b> is specified for <i>fdwOpen</i>.

### -param uDeviceID

Identifier of the waveform-audio input device to open. It can be either a device identifier or a handle of an open waveform-audio input device. You can use the following flag instead of a device identifier.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>WAVE_MAPPER</td>
<td>The function selects a waveform-audio input device capable of recording in the specified format.</td>
</tr>
</table>

### -param pwfx

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that identifies the desired format for recording waveform-audio data. You can free this structure immediately after <b>waveInOpen</b> returns.

### -param dwCallback

Pointer to a fixed callback function, an event handle, a handle to a window, or the identifier of a thread to be called during waveform-audio recording to process messages related to the progress of recording. If no callback function is required, this value can be zero. For more information on the callback function, see <a href="/previous-versions/dd743849(v=vs.85)">waveInProc</a>.

### -param dwInstance

User-instance data passed to the callback mechanism. This parameter is not used with the window callback mechanism.

### -param fdwOpen

Flags for opening the device. The following values are defined.
            

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td><b>CALLBACK_EVENT</b></td>
<td>The <i>dwCallback</i> parameter is an event handle.</td>
</tr>
<tr>
<td><b>CALLBACK_FUNCTION</b></td>
<td>The <i>dwCallback</i> parameter is a callback procedure address.</td>
</tr>
<tr>
<td><b>CALLBACK_NULL</b></td>
<td>No callback mechanism. This is the default setting.</td>
</tr>
<tr>
<td><b>CALLBACK_THREAD</b></td>
<td>The <i>dwCallback</i> parameter is a thread identifier.</td>
</tr>
<tr>
<td><b>CALLBACK_WINDOW</b></td>
<td>The <i>dwCallback</i> parameter is a window handle.</td>
</tr>
<tr>
<td><b>WAVE_MAPPED_DEFAULT_COMMUNICATION_DEVICE</b></td>
<td>
If this flag is specified and the  <i>uDeviceID</i> parameter is <b>WAVE_MAPPER</b>, the function opens the default communication device. 

This flag applies only when <i>uDeviceID</i> equals <b>WAVE_MAPPER</b>.

<div class="alert"><b>Note</b>  Requires Windows 7</div>
<div> </div>
</td>
</tr>
<tr>
<td><b>WAVE_FORMAT_DIRECT</b></td>
<td>If this flag is specified, the ACM driver does not perform conversions on the audio data.</td>
</tr>
<tr>
<td><b>WAVE_FORMAT_QUERY</b></td>
<td>The function queries the device to determine whether it supports the given format, but it does not open the device.</td>
</tr>
<tr>
<td><b>WAVE_MAPPED</b></td>
<td>The <i>uDeviceID</i> parameter specifies a waveform-audio device to be mapped to by the wave mapper.</td>
</tr>
</table>

## -returns

Returns <b>MMSYSERR_NOERROR</b> if successful or an error otherwise. Possible error values include the following.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ALLOCATED</b></dt>
</dl>
</td>
<td width="60%">
Specified resource is already allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
Specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No device driver is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate or lock memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAVERR_BADFORMAT</b></dt>
</dl>
</td>
<td width="60%">
Attempted to open with an unsupported waveform-audio format.

</td>
</tr>
</table>

## -remarks

Use the <a href="/previous-versions/dd743844(v=vs.85)">waveInGetNumDevs</a> function to determine the number of waveform-audio input devices present on the system. The device identifier specified by <i>uDeviceID</i> varies from zero to one less than the number of devices present. The WAVE_MAPPER constant can also be used as a device identifier.
      

If you choose to have a window or thread receive callback information, the following messages are sent to the window procedure or thread to indicate the progress of waveform-audio input: <a href="/windows/desktop/Multimedia/mm-wim-open">MM_WIM_OPEN</a>, <a href="/windows/desktop/Multimedia/mm-wim-close">MM_WIM_CLOSE</a>, and <a href="/windows/desktop/Multimedia/mm-wim-data">MM_WIM_DATA</a>.
      

If you choose to have a function receive callback information, the following messages are sent to the function to indicate the progress of waveform-audio input: <a href="/windows/desktop/Multimedia/wim-open">WIM_OPEN</a>, <a href="/windows/desktop/Multimedia/wim-close">WIM_CLOSE</a>, and <a href="/windows/desktop/Multimedia/wim-data">WIM_DATA</a>.

## -see-also

<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>