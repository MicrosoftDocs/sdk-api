---
UID: NF:mmeapi.midiOutShortMsg
title: midiOutShortMsg function (mmeapi.h)
description: The midiOutShortMsg function sends a short MIDI message to the specified MIDI output device.
helpviewer_keywords: ["_win32_midiOutShortMsg","midiOutShortMsg","midiOutShortMsg function [Windows Multimedia]","mmeapi/midiOutShortMsg","multimedia.midioutshortmsg"]
old-location: multimedia\midioutshortmsg.htm
tech.root: Multimedia
ms.assetid: b46d342a-7bfc-495a-98d3-e0c93ae4fd59
ms.date: 12/05/2018
ms.keywords: _win32_midiOutShortMsg, midiOutShortMsg, midiOutShortMsg function [Windows Multimedia], mmeapi/midiOutShortMsg, multimedia.midioutshortmsg
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
 - midiOutShortMsg
 - mmeapi/midiOutShortMsg
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
 - midiOutShortMsg
---

# midiOutShortMsg function


## -description

The <b>midiOutShortMsg</b> function sends a short MIDI message to the specified MIDI output device.

## -parameters

### -param hmo

Handle to the MIDI output device. This parameter can also be the handle of a MIDI stream cast to <b>HMIDIOUT</b>.

### -param dwMsg

MIDI message. The message is packed into a <b>DWORD</b> value with the first byte of the message in the low-order byte. The message is packed into this parameter as follows.

<table>
<tr>
<th>Word
                </th>
<th>Byte
                </th>
<th>Usage
                </th>
</tr>
<tr>
<td>High</td>
<td>High-order</td>
<td>Not used.</td>
</tr>
<tr>
<td></td>
<td>Low-order</td>
<td>The second byte of MIDI data (when needed).</td>
</tr>
<tr>
<td>Low</td>
<td>High-order</td>
<td>The first byte of MIDI data (when needed).</td>
</tr>
<tr>
<td></td>
<td>Low-order</td>
<td>The MIDI status.</td>
</tr>
</table>
 

The two MIDI data bytes are optional, depending on the MIDI status byte. When a series of messages have the same status byte, the status byte can be omitted from messages after the first one in the series, creating a running status. Pack a message for running status as follows:

<table>
<tr>
<th>Word
                </th>
<th>Byte
                </th>
<th>Usage
                </th>
</tr>
<tr>
<td>High</td>
<td>High-order</td>
<td>Not used.</td>
</tr>
<tr>
<td></td>
<td>Low-order</td>
<td>Not used.</td>
</tr>
<tr>
<td>Low</td>
<td>High-order</td>
<td>The second byte of MIDI data (when needed).</td>
</tr>
<tr>
<td></td>
<td>Low-order</td>
<td>The first byte of MIDI data.</td>
</tr>
</table>

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_BADOPENMODE</b></dt>
</dl>
</td>
<td width="60%">
The application sent a message without a status byte to a stream handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_NOTREADY</b></dt>
</dl>
</td>
<td width="60%">
The hardware is busy with other data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

</td>
</tr>
</table>

## -remarks

This function is used to send any MIDI message except for system-exclusive or stream messages.

This function might not return until the message has been sent to the output device. You can send short messages while streams are playing on the same device (although you cannot use a running status in this case).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>