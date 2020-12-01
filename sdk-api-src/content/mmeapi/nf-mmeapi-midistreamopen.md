---
UID: NF:mmeapi.midiStreamOpen
title: midiStreamOpen function (mmeapi.h)
description: The midiStreamOpen function opens a MIDI stream for output. By default, the device is opened in paused mode. The stream handle retrieved by this function must be used in all subsequent references to the stream.
helpviewer_keywords: ["_win32_midiStreamOpen","midiStreamOpen","midiStreamOpen function [Windows Multimedia]","mmeapi/midiStreamOpen","multimedia.midistreamopen"]
old-location: multimedia\midistreamopen.htm
tech.root: Multimedia
ms.assetid: 355cf034-e1d7-4530-b117-4c505ad0aac6
ms.date: 12/05/2018
ms.keywords: _win32_midiStreamOpen, midiStreamOpen, midiStreamOpen function [Windows Multimedia], mmeapi/midiStreamOpen, multimedia.midistreamopen
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
 - midiStreamOpen
 - mmeapi/midiStreamOpen
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
 - midiStreamOpen
---

# midiStreamOpen function


## -description

The <b>midiStreamOpen</b> function opens a MIDI stream for output. By default, the device is opened in paused mode. The stream handle retrieved by this function must be used in all subsequent references to the stream.

## -parameters

### -param phms

Pointer to a variable to contain the stream handle when the function returns.

### -param puDeviceID

Pointer to a device identifier. The device is opened on behalf of the stream and closed again when the stream is closed.

### -param cMidi

Reserved; must be 1.

### -param dwCallback

Pointer to a callback function, an event handle, a thread identifier, or a handle of a window or thread called during MIDI playback to process messages related to the progress of the playback. If no callback mechanism is desired, specify <b>NULL</b> for this parameter.

### -param dwInstance

Application-specific instance data that is returned to the application with every callback function.

### -param fdwOpen

Callback flag for opening the device. One of the following callback flags must be specified.

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
<td>The <i>dwCallback</i> parameter is a callback procedure address. For the callback signature, see <a href="/previous-versions/dd798478(v=vs.85)">MidiOutProc</a>.</td>
</tr>
<tr>
<td>CALLBACK_NULL</td>
<td>There is no callback mechanism. This is the default setting.</td>
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
The given handle or flags parameter is invalid.

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

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>