---
UID: NF:mmeapi.waveOutOpen
title: waveOutOpen function (mmeapi.h)
description: The waveOutOpen function opens the given waveform-audio output device for playback.
helpviewer_keywords: ["_win32_waveOutOpen","mmeapi/waveOutOpen","multimedia.waveoutopen","waveOutOpen","waveOutOpen function [Windows Multimedia]"]
old-location: multimedia\waveoutopen.htm
tech.root: Multimedia
ms.assetid: ef02221b-df45-4fc3-8d9d-f119fa802d34
ms.date: 12/05/2018
ms.keywords: _win32_waveOutOpen, mmeapi/waveOutOpen, multimedia.waveoutopen, waveOutOpen, waveOutOpen function [Windows Multimedia]
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
 - waveOutOpen
 - mmeapi/waveOutOpen
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
 - waveOutOpen
---

# waveOutOpen function


## -description

The <b>waveOutOpen</b> function opens the given waveform-audio output device for playback.

## -parameters

### -param phwo

Pointer to a buffer that receives a handle identifying the open waveform-audio output device. Use the handle to identify the device when calling other waveform-audio output functions. This parameter might be <b>NULL</b> if the <b>WAVE_FORMAT_QUERY</b> flag is specified for <i>fdwOpen</i>.

### -param uDeviceID

Identifier of the waveform-audio output device to open. It can be either a device identifier or a handle of an open waveform-audio input device. You can also use the following flag instead of a device identifier:

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td><b>WAVE_MAPPER</b></td>
<td>The function selects a waveform-audio output device capable of playing the given format.</td>
</tr>
</table>

### -param pwfx

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that identifies the format of the waveform-audio data to be sent to the device. You can free this structure immediately after passing it to <b>waveOutOpen</b>.

### -param dwCallback

Specifies the callback mechanism. The value must be one of the following:

<ul>
<li>A pointer to a callback function. For the function signature, see <a href="/previous-versions/dd743869(v=vs.85)">waveOutProc</a>.</li>
<li>A handle to a window.</li>
<li>A thread identifier.</li>
<li>A handle to an event.</li>
<li>The value <b>NULL</b>.</li>
</ul>
The <i>fdwOpen</i> parameter specifies how the <i>dwCallback</i> parameter is interpreted. For more information, see Remarks.

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
<td><b>WAVE_ALLOWSYNC</b></td>
<td>If this flag is specified, a synchronous waveform-audio device can be opened. If this flag is not specified while opening a synchronous driver, the device will fail to open.</td>
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
<td>If this flag is specified, <b>waveOutOpen</b> queries the device to determine if it supports the given format, but the device is not actually opened.</td>
</tr>
<tr>
<td><b>WAVE_MAPPED</b></td>
<td>If this flag is specified, the <i>uDeviceID</i> parameter specifies a waveform-audio device to be mapped to by the wave mapper.</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>WAVERR_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The device is synchronous but <a href="/previous-versions/dd743866(v=vs.85)">waveOutOpen</a> was called without using the <b>WAVE_ALLOWSYNC</b> flag.

</td>
</tr>
</table>

## -remarks

Use the <a href="/previous-versions/dd743860(v=vs.85)">waveOutGetNumDevs</a> function to determine the number of waveform-audio output devices present in the system. If the value specified by the <i>uDeviceID</i> parameter is a device identifier, it can vary from zero to one less than the number of devices present. The <b>WAVE_MAPPER</b> constant can also be used as a device identifier.
      

The structure pointed to by <i>pwfx</i> can be extended to include type-specific information for certain data formats. For example, for PCM data, an extra <b>UINT</b> is added to specify the number of bits per sample. Use the <a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a> structure in this case. For all other waveform-audio formats, use the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure to specify the length of the additional data.

If you choose to have a window or thread receive callback information, the following messages are sent to the window procedure function to indicate the progress of waveform-audio output: <a href="/windows/desktop/Multimedia/mm-wom-open">MM_WOM_OPEN</a>, <a href="/windows/desktop/Multimedia/mm-wom-close">MM_WOM_CLOSE</a>, and <a href="/windows/desktop/Multimedia/mm-wom-done">MM_WOM_DONE</a>.
      

<h3><a id="Callback_Mechanism"></a><a id="callback_mechanism"></a><a id="CALLBACK_MECHANISM"></a>Callback Mechanism</h3>
The <i>dwCallback</i> and <i>fdwOpen</i> parameters specify how the application is notified about  the progress of waveform-audio output.

If <i>fdwOpen</i> contains the <b>CALLBACK_FUNCTION</b> flag, <i>dwCallback</i> is a pointer to a callback function. For the function signature, see <a href="/previous-versions/dd743869(v=vs.85)">waveOutProc</a>. The <i>uMsg</i> parameter of the callback indicates the progress of the audio output:

<ul>
<li>
<a href="/windows/desktop/Multimedia/wom-open">WOM_OPEN</a>
</li>
<li>
<a href="/windows/desktop/Multimedia/wom-close">WOM_CLOSE</a>
</li>
<li>
<a href="/windows/desktop/Multimedia/wom-done">WOM_DONE</a>
</li>
</ul>
If <i>fdwOpen</i> contains the <b>CALLBACK_WINDOW</b> flag, <i>dwCallback</i> is a handle to a window.The window receives the following messages, indicating the progress:

<ul>
<li>
<a href="/windows/desktop/Multimedia/mm-wom-open">MM_WOM_OPEN</a>
</li>
<li>
<a href="/windows/desktop/Multimedia/mm-wom-close">MM_WOM_CLOSE</a>
</li>
<li>
<a href="/windows/desktop/Multimedia/mm-wom-done">MM_WOM_DONE</a>
</li>
</ul>
 If <i>fdwOpen</i> contains the <b>CALLBACK_THREAD</b> flag, <i>dwCallback</i> is a thread identifier. The thread receives the messages listed previously for <b>CALLBACK_WINDOW</b>.

If <i>fdwOpen</i> contains the <b>CALLBACK_EVENT</b> flag, <i>dwCallback</i> is a handle to an event. The event is signaled whenever the state of the waveform buffer changes. The application can use <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects">WaitForMultipleObjects</a> to wait for the event. When the event is signaled, you can get the current state of the waveform buffer by checking the <b>dwFlags</b> member of the <a href="/previous-versions/dd743837(v=vs.85)">WAVEHDR</a> structure. (See <a href="/previous-versions/dd743868(v=vs.85)">waveOutPrepareHeader</a>.)

If <i>fdwOpen</i> contains the <b>CALLBACK_NULL</b> flag, <i>dwCallback</i> must be <b>NULL</b>. In that case, no callback mechanism is used.

## -see-also

<a href="/windows/desktop/Multimedia/using-a-callback-function-to-process-driver-messages">Using a Callback Function to Process Driver Messages</a>



<a href="/windows/desktop/Multimedia/using-a-window-or-thread-to-process-driver-messages">Using a Window or Thread to Process Driver Messages</a>



<a href="/windows/desktop/Multimedia/using-an-callback-to-process-driver-messages">Using an Event Callback to Process Driver Messages</a>



<a href="/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>