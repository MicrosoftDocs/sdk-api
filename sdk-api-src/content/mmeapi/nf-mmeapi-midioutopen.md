---
UID: NF:mmeapi.midiOutOpen
title: midiOutOpen function (mmeapi.h)
description: The midiOutOpen function opens a MIDI output device for playback.
helpviewer_keywords: ["_win32_midiOutOpen","midiOutOpen","midiOutOpen function [Windows Multimedia]","mmeapi/midiOutOpen","multimedia.midioutopen"]
old-location: multimedia\midioutopen.htm
tech.root: Multimedia
ms.assetid: 929cd4d1-6912-4456-a6c7-24a819799e46
ms.date: 12/05/2018
ms.keywords: _win32_midiOutOpen, midiOutOpen, midiOutOpen function [Windows Multimedia], mmeapi/midiOutOpen, multimedia.midioutopen
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
 - midiOutOpen
 - mmeapi/midiOutOpen
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
 - midiOutOpen
---

# midiOutOpen function


## -description

The <b>midiOutOpen</b> function opens a MIDI output device for playback.

## -parameters

### -param phmo

Pointer to an <b>HMIDIOUT</b> handle. This location is filled with a handle identifying the opened MIDI output device. The handle is used to identify the device in calls to other MIDI output functions.

### -param uDeviceID

Identifier of the MIDI output device that is to be opened.

### -param dwCallback

Pointer to a callback function, an event handle, a thread identifier, or a handle of a window or thread called during MIDI playback to process messages related to the progress of the playback. If no callback is desired, specify <b>NULL</b> for this parameter. For more information on the callback function, see <a href="/previous-versions/dd798478(v=vs.85)">MidiOutProc</a>.

### -param dwInstance

User instance data passed to the callback. This parameter is not used with window callbacks or threads.

### -param fdwOpen

Callback flag for opening the device. It can be the following values.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>CALLBACK_EVENT</td>
<td>The <i>dwCallback</i> parameter is an event handle. This callback mechanism is for output only.</td>
</tr>
<tr>
<td>CALLBACK_FUNCTION</td>
<td>The <i>dwCallback</i> parameter is a callback function address.</td>
</tr>
<tr>
<td>CALLBACK_NULL</td>
<td>There is no callback mechanism. This value is the default setting.</td>
</tr>
<tr>
<td>CALLBACK_THREAD</td>
<td>The <i>dwCallback</i> parameter is a thread identifier.</td>
</tr>
<tr>
<td>CALLBACK_WINDOW</td>
<td>The <i>dwCallback</i> parameter is a window handle.</td>
</tr>
</table>

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_NODEVICE</b></dt>
</dl>
</td>
<td width="60%">
No MIDI port was found. This error occurs only when the mapper is opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ALLOCATED</b></dt>
</dl>
</td>
<td width="60%">
The specified resource is already allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
The specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer or structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
</table>

## -remarks

To determine the number of MIDI output devices present in the system, use the <a href="/previous-versions/dd798472(v=vs.85)">midiOutGetNumDevs</a> function. The device identifier specified by <i>wDeviceID</i> varies from zero to one less than the number of devices present. MIDI_MAPPER can also be used as the device identifier.

If a window or thread is chosen to receive callback information, the following messages are sent to the window procedure or thread to indicate the progress of MIDI output: <a href="/windows/desktop/Multimedia/mm-mom-open">MM_MOM_OPEN</a>, <a href="/windows/desktop/Multimedia/mm-mom-close">MM_MOM_CLOSE</a>, and <a href="/windows/desktop/Multimedia/mm-mom-done">MM_MOM_DONE</a>.

If a function is chosen to receive callback information, the following messages are sent to the function to indicate the progress of MIDI output: <a href="/windows/desktop/Multimedia/mom-open">MOM_OPEN</a>, <a href="/windows/desktop/Multimedia/mom-close">MOM_CLOSE</a>, and <a href="/windows/desktop/Multimedia/mom-done">MOM_DONE</a>.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>