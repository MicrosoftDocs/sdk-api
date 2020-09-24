---
UID: NS:mmeapi.midihdr_tag
title: MIDIHDR (mmeapi.h)
description: The MIDIHDR structure defines the header used to identify a MIDI system-exclusive or stream buffer.
helpviewer_keywords: ["*LPMIDIHDR","*NPMIDIHDR","*PMIDIHDR","LPMIDIHDR","LPMIDIHDR structure pointer [Windows Multimedia]","MHDR_DONE","MHDR_INQUEUE","MHDR_ISSTRM","MHDR_PREPARED","MIDIHDR","MIDIHDR structure [Windows Multimedia]","_win32_MIDIHDR_str","midihdr_tag","mmeapi/LPMIDIHDR","mmeapi/MIDIHDR","multimedia.midihdr"]
old-location: multimedia\midihdr.htm
tech.root: Multimedia
ms.assetid: 630f0645-555e-4f48-9397-2623a9918b8a
ms.date: 12/05/2018
ms.keywords: '*LPMIDIHDR, *NPMIDIHDR, *PMIDIHDR, LPMIDIHDR, LPMIDIHDR structure pointer [Windows Multimedia], MHDR_DONE, MHDR_INQUEUE, MHDR_ISSTRM, MHDR_PREPARED, MIDIHDR, MIDIHDR structure [Windows Multimedia], _win32_MIDIHDR_str, midihdr_tag, mmeapi/LPMIDIHDR, mmeapi/MIDIHDR, multimedia.midihdr'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIDIHDR, *PMIDIHDR, *NPMIDIHDR, *LPMIDIHDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midihdr_tag
 - mmeapi/midihdr_tag
 - PMIDIHDR
 - mmeapi/PMIDIHDR
 - MIDIHDR
 - mmeapi/MIDIHDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - MIDIHDR
---

# MIDIHDR structure


## -description

The <b>MIDIHDR</b> structure defines the header used to identify a MIDI system-exclusive or stream buffer.

## -struct-fields

### -field lpData

Pointer to MIDI data.

### -field dwBufferLength

Size of the buffer.

### -field dwBytesRecorded

Actual amount of data in the buffer. This value should be less than or equal to the value given in the <b>dwBufferLength</b> member.

### -field dwUser

Custom user data.

### -field dwFlags

Flags giving information about the buffer.

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MHDR_DONE"></a><a id="mhdr_done"></a><dl>
<dt><b>MHDR_DONE</b></dt>
</dl>
</td>
<td width="60%">
Set by the device driver to indicate that it is finished with the buffer and is returning it to the application.

</td>
</tr>
<tr>
<td width="40%"><a id="MHDR_INQUEUE"></a><a id="mhdr_inqueue"></a><dl>
<dt><b>MHDR_INQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Set by Windows to indicate that the buffer is queued for playback.

</td>
</tr>
<tr>
<td width="40%"><a id="MHDR_ISSTRM"></a><a id="mhdr_isstrm"></a><dl>
<dt><b>MHDR_ISSTRM</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate that the buffer is a stream buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="MHDR_PREPARED"></a><a id="mhdr_prepared"></a><dl>
<dt><b>MHDR_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
Set by Windows to indicate that the buffer has been prepared by using the <a href="/previous-versions/dd798459(v=vs.85)">midiInPrepareHeader</a> or <a href="/previous-versions/dd798477(v=vs.85)">midiOutPrepareHeader</a> function.

</td>
</tr>
</table>

### -field lpNext

Reserved; do not use.

### -field reserved

Reserved; do not use.

### -field dwOffset

Offset into the buffer when a callback is performed. (This callback is generated because the MEVT_F_CALLBACK flag is set in the <b>dwEvent</b> member of the <a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> structure.) This offset enables an application to determine which event caused the callback.

### -field dwReserved

Reserved; do not use.

## -see-also

MIDI Structures



<a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>



<a href="/previous-versions/dd798459(v=vs.85)">midiInPrepareHeader</a>



<a href="/previous-versions/dd798477(v=vs.85)">midiOutPrepareHeader</a>