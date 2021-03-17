---
UID: NF:mmeapi.midiOutClose
title: midiOutClose function (mmeapi.h)
description: The midiOutClose function closes the specified MIDI output device.
helpviewer_keywords: ["_win32_midiOutClose","midiOutClose","midiOutClose function [Windows Multimedia]","mmeapi/midiOutClose","multimedia.midioutclose"]
old-location: multimedia\midioutclose.htm
tech.root: Multimedia
ms.assetid: 4f23295c-1c2c-4060-9c19-b3f0ed5bf44c
ms.date: 12/05/2018
ms.keywords: _win32_midiOutClose, midiOutClose, midiOutClose function [Windows Multimedia], mmeapi/midiOutClose, multimedia.midioutclose
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
 - midiOutClose
 - mmeapi/midiOutClose
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
 - midiOutClose
---

# midiOutClose function


## -description

The <b>midiOutClose</b> function closes the specified MIDI output device.

## -parameters

### -param hmo

Handle to the MIDI output device. If the function is successful, the handle is no longer valid after the call to this function.

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
<dt><b>MIDIERR_STILLPLAYING</b></dt>
</dl>
</td>
<td width="60%">
Buffers are still in the queue.

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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to load mapper string description.

</td>
</tr>
</table>

## -remarks

If there are output buffers that have been sent by using the <a href="/previous-versions/dd798474(v=vs.85)">midiOutLongMsg</a> function and have not been returned to the application, the close operation will fail. To mark all pending buffers as being done, use the <a href="/previous-versions/dd798479(v=vs.85)">midiOutReset</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>