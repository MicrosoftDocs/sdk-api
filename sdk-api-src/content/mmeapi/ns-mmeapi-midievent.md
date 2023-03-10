---
UID: NS:mmeapi.midievent_tag
title: MIDIEVENT (mmeapi.h)
description: The MIDIEVENT structure describes a MIDI event in a stream buffer.
helpviewer_keywords: ["MIDIEVENT","MIDIEVENT structure [Windows Multimedia]","_win32_MIDIEVENT_str","midievent_tag","mmeapi/MIDIEVENT","multimedia.midievent"]
old-location: multimedia\midievent.htm
tech.root: Multimedia
ms.assetid: e83bf111-2075-4cfc-a68b-e0a59a0c53e6
ms.date: 12/05/2018
ms.keywords: MIDIEVENT, MIDIEVENT structure [Windows Multimedia], _win32_MIDIEVENT_str, midievent_tag, mmeapi/MIDIEVENT, multimedia.midievent
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
req.typenames: MIDIEVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - midievent_tag
 - mmeapi/midievent_tag
 - MIDIEVENT
 - mmeapi/MIDIEVENT
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
 - MIDIEVENT
---

# MIDIEVENT structure


## -description

The MIDIEVENT structure describes a MIDI event in a stream buffer.

## -struct-fields

### -field dwDeltaTime

Time, in MIDI ticks, between the previous event and the current event. The length of a tick is defined by the time format and possibly the tempo associated with the stream. (The definition is identical to the specification for a tick in a standard MIDI file.)

### -field dwStreamID

Reserved; must be zero.

### -field dwEvent

Event code and event parameters or length. To parse this information, use the <a href="/previous-versions/dd798442(v=vs.85)">MEVT_EVENTTYPE</a> and <a href="/previous-versions/dd798441(v=vs.85)">MEVT_EVENTPARM</a> macros. See Remarks.

### -field dwParms

If <b>dwEvent</b> specifies MEVT_F_LONG and the length of the buffer, this member contains parameters for the event. This parameter data must be padded with zeros so that an integral number of <b>DWORD</b> values are stored. For example, if the event data is five bytes long, three pad bytes must follow the data for a total of eight bytes. In this case, the low 24 bits of <b>dwEvent</b> would contain the value 5.
            

If <b>dwEvent</b> specifies MEVT_F_SHORT, do not use this member in the stream buffer.

## -remarks

The high byte of <b>dwEvent</b> contains flags and an event code. Either the MEVT_F_LONG or MEVT_F_SHORT flag must be specified. The MEVT_F_CALLBACK flag is optional. The following table describes these flags.
      

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>MEVT_F_CALLBACK</td>
<td>The system generates a callback when the event
              is about to be executed.
            </td>
</tr>
<tr>
<td>MEVT_F_LONG</td>
<td>The event is a long event. The low 24 bits of dwEvent contain the length of the event parameters included in dwParms.
            </td>
</tr>
<tr>
<td>MEVT_F_SHORT</td>
<td>The event is a short event. The event parameters are contained in the low 24 bits of dwEvent.</td>
</tr>
</table>
 

The remainder of the high byte contains one of the following event codes:
      

<table>
<tr>
<th>Event Code</th>
<th>Meaning</th>
</tr>
<tr>
<td>MEVT_COMMENT</td>
<td>Long event. The event data will be ignored. This event is intended to store commentary information about the stream that might be useful to authoring programs or sequencers if the stream data were to be stored in a file in stream format. In a buffer of this data, the zero byte identifies the comment class and subsequent bytes contain the comment data. </td>
</tr>
<tr>
<td>MEVT_LONGMSG</td>
<td>Long event. The event data is transmitted verbatim. The event data is assumed to be system-exclusive data; that is, running status will be cleared when the event is executed and running status from any previous events will not be applied to any channel events in the event data. Using this event to send a group of channel messages at the same time is not recommended; a set of MEVT_SHORTMSG events with zero delta times should be used instead.</td>
</tr>
<tr>
<td>MEVT_NOP</td>
<td>Short event. This event is a placeholder; it does nothing. The low 24 bits are ignored. This event will still generate a callback if MEVT_F_CALLBACK is set in dwEvent.</td>
</tr>
<tr>
<td>MEVT_SHORTMSG</td>
<td>Short event. The data in the low 24 bits of dwEvent is a MIDI short message. (For a description of how a short message is packed into a DWORD value, see the midiOutShortMsg function.)</td>
</tr>
<tr>
<td>MEVT_TEMPO</td>
<td>Short event. The data in the low 24 bits of dwEvent contain the new tempo for following events. The tempo is specified in the same format as it is for the tempo change meta-event in a MIDI file — that is, in microseconds per quarter note. (This event will have no effect if the time format specified for the stream is SMPTE time.)</td>
</tr>
<tr>
<td>MEVT_VERSION</td>
<td>Long event. The event data must contain a MIDISTRMBUFFVER structure.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/dd798441(v=vs.85)">MEVT_EVENTPARM</a>



<a href="/previous-versions/dd798442(v=vs.85)">MEVT_EVENTTYPE</a>



<a href="/windows/desktop/Multimedia/midi-structures">MIDI Structures</a>



<a href="/previous-versions/dd798493(v=vs.85)">MIDISTRMBUFFVER</a>



<a href="/windows/desktop/Multimedia/musical-instrument-digital-interface--midi">Musical Instrument Digital Interface (MIDI)</a>



<a href="/previous-versions/dd798481(v=vs.85)">midiOutShortMsg</a>