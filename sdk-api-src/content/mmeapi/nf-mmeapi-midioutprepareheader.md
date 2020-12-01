---
UID: NF:mmeapi.midiOutPrepareHeader
title: midiOutPrepareHeader function (mmeapi.h)
description: The midiOutPrepareHeader function prepares a MIDI system-exclusive or stream buffer for output.
helpviewer_keywords: ["_win32_midiOutPrepareHeader","midiOutPrepareHeader","midiOutPrepareHeader function [Windows Multimedia]","mmeapi/midiOutPrepareHeader","multimedia.midioutprepareheader"]
old-location: multimedia\midioutprepareheader.htm
tech.root: Multimedia
ms.assetid: 3e457f08-a885-48f8-97c1-ba1baef97759
ms.date: 12/05/2018
ms.keywords: _win32_midiOutPrepareHeader, midiOutPrepareHeader, midiOutPrepareHeader function [Windows Multimedia], mmeapi/midiOutPrepareHeader, multimedia.midioutprepareheader
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
 - midiOutPrepareHeader
 - mmeapi/midiOutPrepareHeader
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
 - midiOutPrepareHeader
---

# midiOutPrepareHeader function


## -description

The <b>midiOutPrepareHeader</b> function prepares a MIDI system-exclusive or stream buffer for output.

## -parameters

### -param hmo

Handle to the MIDI output device. To get the device handle, call <a href="/previous-versions/dd798476(v=vs.85)">midiOutOpen</a>. This parameter can also be the handle of a MIDI stream cast to a <b>HMIDIOUT</b> type.

### -param pmh

Pointer to a <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure that identifies the buffer to be prepared.
          

Before calling the function, set the <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members of the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure. The <b>dwFlags</b> member must be set to zero.

### -param cbmh

Size, in bytes, of the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure.

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
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified address is invalid or the given stream buffer is greater than 64K.

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

Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the <b>midiOutPrepareHeader</b> function. After the header has been prepared, do not modify the buffer. After the driver is done using the buffer, call the <a href="/previous-versions/dd798482(v=vs.85)">midiOutUnprepareHeader</a> function.

The application can re-use the same buffer, or allocate multiple buffers and  call <b>midiOutPrepareHeader</b> for each buffer. If you re-use the same buffer, it is not necessary to prepare the buffer each time. You can call  <b>midiOutPrepareHeader</b> once at the beginning and then call <a href="/previous-versions/dd798482(v=vs.85)">midiOutUnprepareHeader</a> once at the end.

A stream buffer cannot be larger than 64K.
      

Preparing a header that has already been prepared has no effect, and the function returns MMSYSERR_NOERROR.

## -see-also

<a href="/windows/desktop/Multimedia/allocating-and-preparing-midi-data-blocks">Allocating and Preparing MIDI Data Blocks</a>



<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>



<a href="/previous-versions/dd798482(v=vs.85)">midiOutUnprepareHeader</a>