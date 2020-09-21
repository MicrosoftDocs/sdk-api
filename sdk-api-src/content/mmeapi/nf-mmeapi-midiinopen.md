---
UID: NF:mmeapi.midiInOpen
title: midiInOpen function (mmeapi.h)
description: The midiInOpen function opens a specified MIDI input device.
helpviewer_keywords: ["_win32_midiInOpen","midiInOpen","midiInOpen function [Windows Multimedia]","mmeapi/midiInOpen","multimedia.midiinopen"]
old-location: multimedia\midiinopen.htm
tech.root: Multimedia
ms.assetid: 230deaef-9473-426f-a0eb-14e259600e68
ms.date: 12/05/2018
ms.keywords: _win32_midiInOpen, midiInOpen, midiInOpen function [Windows Multimedia], mmeapi/midiInOpen, multimedia.midiinopen
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
 - midiInOpen
 - mmeapi/midiInOpen
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
 - midiInOpen
---

# midiInOpen function


## -description

The <b>midiInOpen</b> function opens a specified MIDI input device.

## -parameters

### -param phmi

Pointer to an <b>HMIDIIN</b> handle. This location is filled with a handle identifying the opened MIDI input device. The handle is used to identify the device in calls to other MIDI input functions.

### -param uDeviceID

Identifier of the MIDI input device to be opened.

### -param dwCallback

Pointer to a callback function, a thread identifier, or a handle of a window called with information about incoming MIDI messages. For more information on the callback function, see <a href="/previous-versions/dd798460(v=vs.85)">MidiInProc</a>.

### -param dwInstance

User instance data passed to the callback function. This parameter is not used with window callback functions or threads.

### -param fdwOpen

Callback flag for opening the device and, optionally, a status flag that helps regulate rapid data transfers. It can be the following values.

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>CALLBACK_FUNCTION</td>
<td>The <i>dwCallback</i> parameter is a callback procedure address.</td>
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
<tr>
<td>MIDI_IO_STATUS</td>
<td>When this parameter also specifies CALLBACK_FUNCTION, <a href="/windows/desktop/Multimedia/mim-moredata">MIM_MOREDATA</a> messages are sent to the callback function as well as <a href="/windows/desktop/Multimedia/mim-data">MIM_DATA</a> messages. Or, if this parameter also specifies CALLBACK_WINDOW, <a href="/windows/desktop/Multimedia/mm-mim-moredata">MM_MIM_MOREDATA</a> messages are sent to the window as well as <a href="/windows/desktop/Multimedia/mm-mim-data">MM_MIM_DATA</a> messages. This flag does not affect event or thread callbacks.</td>
</tr>
</table>
 

Most applications that use a callback mechanism will specify CALLBACK_FUNCTION for this parameter.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following/

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
<dt><b>MMSYSERR_INVALFLAG</b></dt>
</dl>
</td>
<td width="60%">
The flags specified by <i>dwFlags</i> are invalid.

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

To determine the number of MIDI input devices present in the system, use the <a href="/previous-versions/dd798456(v=vs.85)">midiInGetNumDevs</a> function. The device identifier specified by <i>wDeviceID</i> varies from zero to one less than the number of devices present.

If a window or thread is chosen to receive callback information, the following messages are sent to the window procedure or thread to indicate the progress of MIDI input: <a href="/windows/desktop/Multimedia/mm-mim-open">MM_MIM_OPEN</a>, <a href="/windows/desktop/Multimedia/mm-mim-close">MM_MIM_CLOSE</a>, <a href="/windows/desktop/Multimedia/mm-mim-data">MM_MIM_DATA</a>, <a href="/windows/desktop/Multimedia/mm-mim-longdata">MM_MIM_LONGDATA</a>, <a href="/windows/desktop/Multimedia/mm-mim-error">MM_MIM_ERROR</a>, <a href="/windows/desktop/Multimedia/mm-mim-longerror">MM_MIM_LONGERROR</a>, and <a href="/windows/desktop/Multimedia/mm-mim-moredata">MM_MIM_MOREDATA</a>.

If a function is chosen to receive callback information, the following messages are sent to the function to indicate the progress of MIDI input: <a href="/windows/desktop/Multimedia/mim-open">MIM_OPEN</a>, <a href="/windows/desktop/Multimedia/mim-close">MIM_CLOSE</a>, <a href="/windows/desktop/Multimedia/mim-data">MIM_DATA</a>, <a href="/windows/desktop/Multimedia/mim-longdata">MIM_LONGDATA</a>, <a href="/windows/desktop/Multimedia/mim-error">MIM_ERROR</a>, <a href="/windows/desktop/Multimedia/mim-longerror">MIM_LONGERROR</a>, and <a href="/windows/desktop/Multimedia/mim-moredata">MIM_MOREDATA</a>.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>