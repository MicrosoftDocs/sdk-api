---
UID: NF:sbe.ISBE2SpanningEvent.GetEvent
title: ISBE2SpanningEvent::GetEvent (sbe.h)
description: Gets an in-band spanning event and event data from the Stream Buffer Engine, version 2 (SBE2). An in-band spanning event is an event that exists until it is replaced or erased, and is part of the state for events that appear later in the same stream.
helpviewer_keywords: ["GetEvent","GetEvent method [Microsoft TV Technologies]","GetEvent method [Microsoft TV Technologies]","ISBE2SpanningEvent interface","ISBE2SpanningEvent interface [Microsoft TV Technologies]","GetEvent method","ISBE2SpanningEvent.GetEvent","ISBE2SpanningEvent::GetEvent","mstv.isbe2spanningevent_getevent","sbe/ISBE2SpanningEvent::GetEvent"]
old-location: mstv\isbe2spanningevent_getevent.htm
tech.root: mstv
ms.assetid: f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef
ms.date: 12/05/2018
ms.keywords: GetEvent, GetEvent method [Microsoft TV Technologies], GetEvent method [Microsoft TV Technologies],ISBE2SpanningEvent interface, ISBE2SpanningEvent interface [Microsoft TV Technologies],GetEvent method, ISBE2SpanningEvent.GetEvent, ISBE2SpanningEvent::GetEvent, mstv.isbe2spanningevent_getevent, sbe/ISBE2SpanningEvent::GetEvent
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISBE2SpanningEvent::GetEvent
 - sbe/ISBE2SpanningEvent::GetEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2SpanningEvent.GetEvent
---

# ISBE2SpanningEvent::GetEvent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an in-band spanning event and  event data from the Stream Buffer Engine, version 2 (SBE2). An <i>in-band spanning event</i> is an event that exists until it is replaced or erased, and is part of the state for events that appear later in the same stream.

## -parameters

### -param idEvt [in]

GUID identifying the spanning event type.

### -param streamId [in]

Identifies the stream containing the spanning event.

### -param pcb [in, out]

Pointer to a value that gets the size of the event data buffer. If the <i>pb</i> parameter is <b>NULL</b>, this parameter returns the required buffer size.

### -param pb [out]

Pointer to a buffer that gets the event data. If this parameter is <b>NULL</b>, the <i>pcb</i> parameter returns the required buffer size. The structure of the event data depends on the event type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following types of in-band spanning events are defined.


<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>EVENTID_ARIBcontentSpanningEvent</td>
<td>Signals the start of Integrated Services Digital Broadcasting (ISDB) content. No data is associated with this event.</td>
</tr>
<tr>
<td>EVENTID_AudioDescriptorSpanningEvent</td>
<td>Contains an MPEG-2 descriptor for an audio stream. The event data is a byte array with the following layout:<ul>
<li>Byte 0 contains the descriptor tag.</li>
<li>Byte 1 contains the length of the descriptor body.</li>
<li>The remaining bytes contain the descriptor body.</li>
</ul>
</td>
</tr>
<tr>
<td>EVENTID_AudioTypeSpanningEvent</td>
<td>Specifies the audio type of the data stream. The event data is a <b>char</b> that contains the audio_type field from the ISO 639 Language Descriptor.</td>
</tr>
<tr>
<td>EVENTID_CASFailureSpanningEvent</td>
<td>Signals a failure in the condition access system (CAS). The event data depends on the CAS technology in use. </td>
</tr>
<tr>
<td>EVENTID_ChannelChangeSpanningEvent</td>
<td>Signals the start or end of a channel change. The event data is a <a href="/previous-versions/windows/desktop/mstv/channelchangeinfo">ChannelChangeInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_ChannelInfoSpanningEvent</td>
<td>Contains information about the cable television channel. The event data is a <a href="/previous-versions/windows/desktop/mstv/channelinfo">ChannelInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_ChannelTypeSpanningEvent</td>
<td>Contains information about the cable television channel type. The event data is a <a href="/previous-versions/windows/desktop/mstv/channelinfo">ChannelTypeInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_CSDescriptorSpanningEvent</td>
<td>Contains a caption service descriptor. The event data is a <a href="/previous-versions/windows/desktop/mstv/spanningeventdescriptor">SpanningEventDescriptor</a> structure.</td>
</tr>
<tr>
<td>EVENTID_CtxADescriptorSpanningEvent</td>
<td>Contains a content advisory descriptor. The event data is a <a href="/previous-versions/windows/desktop/mstv/spanningeventdescriptor">SpanningEventDescriptor</a> structure.</td>
</tr>
<tr>
<td>EVENTID_DualMonoSpanningEvent</td>
<td>Specifies the audio languages for a dual-mono audio stream. The event data is a <a href="/previous-versions/windows/desktop/mstv/dualmonoinfo">DualMonoInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_DVBScramblingControlSpanningEvent</td>
<td>Indicates whether a Digital Video Broadcasting (DVB) program stream is scrambled. This event is signaled when the value of the transport_scrambling_control field changes. The event data is a <a href="/previous-versions/windows/desktop/mstv/dvbscramblingcontrolspanningevent">DVBScramblingControlSpanningEvent</a> structure.</td>
</tr>
<tr>
<td>EVENTID_EmmMessageSpanningEvent</td>
<td>Contains information about an Entitlement Management Message (EMM) in a DVB data stream. The event data is a <a href="/previous-versions/windows/desktop/mstv/spanningeventemmmessage">SpanningEventEmmMessage</a> structure.</td>
</tr>
<tr>
<td>EVENTID_LanguageSpanningEvent</td>
<td>Specifies the audio language. The event data is a <a href="/previous-versions/windows/desktop/mstv/languageinfo">LanguageInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_PBDAParentalControlSpanningEvent</td>
<td>Contains information about the current parental control policy. The event data is a <a href="/previous-versions/windows/desktop/mstv/pbdaparentalcontrol">PBDAParentalControl</a> structure.</td>
</tr>
<tr>
<td>EVENTID_PIDListSpanningEvent</td>
<td>Contains a list of packet identifiers (PIDs) for the current stream. The event data is a <a href="/previous-versions/windows/desktop/mstv/pidlistspanningevent">PIDListSpanningEvent</a> structure.</td>
</tr>
<tr>
<td>EVENTID_RRTSpanningEvent</td>
<td>Contains information about a rating region table (RRT). The data is a <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-section">SECTION</a> structure.</td>
</tr>
<tr>
<td>EVENTID_SignalAndServiceStatusSpanningEvent</td>
<td>Signals the current state of the television service. The event data is a member of the <a href="/previous-versions/windows/desktop/mstv/signalandservicestatusspanningevent-state">SignalAndServiceStatusSpanningEvent_State</a> enumeration.</td>
</tr>
<tr>
<td>EVENTID_StreamIDSpanningEvent</td>
<td>Contains a stream identifier descriptor.  The event data has the same format as the EVENTID_AudioDescriptorSpanningEvent event.</td>
</tr>
<tr>
<td>EVENTID_StreamTypeSpanningEvent</td>
<td>Specifies the stream type. The event data is a <b>DWORD</b> that contains a value from the <a href="/previous-versions/windows/desktop/mstv/mpeg2streamtype">MPEG2StreamType</a> enumeration.</td>
</tr>
<tr>
<td>EVENTID_SubtitleSpanningEvent</td>
<td>Contains a subtitling descriptor. The event data has the same format as the <b>EVENTID_AudioDescriptorSpanningEvent</b> event.</td>
</tr>
<tr>
<td>EVENTID_TeletextSpanningEvent</td>
<td>Contains a teletext descriptor. The event data has the same format as the <b>EVENTID_AudioDescriptorSpanningEvent</b> event.</td>
</tr>
<tr>
<td>EVENTID_TuneFailureSpanningEvent</td>
<td>Signals a tuning failure.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2spanningevent">ISBE2SpanningEvent</a>



<a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2spanningevent-getevent">ISBE2SpanningEvent::GetEvent</a>