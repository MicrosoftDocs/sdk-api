---
UID: NF:sbe.ISBE2SpanningEvent.GetEvent
title: ISBE2SpanningEvent::GetEvent
author: windows-sdk-content
description: Gets an in-band spanning event and event data from the Stream Buffer Engine, version 2 (SBE2). An in-band spanning event is an event that exists until it is replaced or erased, and is part of the state for events that appear later in the same stream.
old-location: mstv\isbe2spanningevent_getevent.htm
tech.root: MSTV
ms.assetid: f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetEvent, GetEvent method [Microsoft TV Technologies], GetEvent method [Microsoft TV Technologies],ISBE2SpanningEvent interface, ISBE2SpanningEvent interface [Microsoft TV Technologies],GetEvent method, ISBE2SpanningEvent.GetEvent, ISBE2SpanningEvent::GetEvent, mstv.isbe2spanningevent_getevent, sbe/ISBE2SpanningEvent::GetEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2SpanningEvent.GetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISBE2SpanningEvent::GetEvent


## -description


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




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
<td>Signals the start or end of a channel change. The event data is a <a href="https://msdn.microsoft.com/61130e8e-7000-4f5a-b4c1-7ae22cfad473">ChannelChangeInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_ChannelInfoSpanningEvent</td>
<td>Contains information about the cable television channel. The event data is a <a href="https://msdn.microsoft.com/4d4c8e5b-5b9f-4cff-98c7-6d3645e677e1">ChannelInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_ChannelTypeSpanningEvent</td>
<td>Contains information about the cable television channel type. The event data is a <a href="https://msdn.microsoft.com/4d4c8e5b-5b9f-4cff-98c7-6d3645e677e1">ChannelTypeInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_CSDescriptorSpanningEvent</td>
<td>Contains a caption service descriptor. The event data is a <a href="https://msdn.microsoft.com/d394b0c9-a61a-44e8-972d-0c12fd446e59">SpanningEventDescriptor</a> structure.</td>
</tr>
<tr>
<td>EVENTID_CtxADescriptorSpanningEvent</td>
<td>Contains a content advisory descriptor. The event data is a <a href="https://msdn.microsoft.com/d394b0c9-a61a-44e8-972d-0c12fd446e59">SpanningEventDescriptor</a> structure.</td>
</tr>
<tr>
<td>EVENTID_DualMonoSpanningEvent</td>
<td>Specifies the audio languages for a dual-mono audio stream. The event data is a <a href="https://msdn.microsoft.com/dd3b702b-1017-4963-91ba-516a3bbb3b60">DualMonoInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_DVBScramblingControlSpanningEvent</td>
<td>Indicates whether a Digital Video Broadcasting (DVB) program stream is scrambled. This event is signaled when the value of the transport_scrambling_control field changes. The event data is a <a href="https://msdn.microsoft.com/e54e8ab2-fc90-4540-aed1-c6dedc2f5d88">DVBScramblingControlSpanningEvent</a> structure.</td>
</tr>
<tr>
<td>EVENTID_EmmMessageSpanningEvent</td>
<td>Contains information about an Entitlement Management Message (EMM) in a DVB data stream. The event data is a <a href="https://msdn.microsoft.com/e362a3b5-db4a-4a58-adf9-d799f83c9f36">SpanningEventEmmMessage</a> structure.</td>
</tr>
<tr>
<td>EVENTID_LanguageSpanningEvent</td>
<td>Specifies the audio language. The event data is a <a href="https://msdn.microsoft.com/25c936a7-b4d6-4af9-a8cc-7af5aed5b23e">LanguageInfo</a> structure.</td>
</tr>
<tr>
<td>EVENTID_PBDAParentalControlSpanningEvent</td>
<td>Contains information about the current parental control policy. The event data is a <a href="https://msdn.microsoft.com/4086651b-45b3-4896-9ae2-6db7e121eb5e">PBDAParentalControl</a> structure.</td>
</tr>
<tr>
<td>EVENTID_PIDListSpanningEvent</td>
<td>Contains a list of packet identifiers (PIDs) for the current stream. The event data is a <a href="https://msdn.microsoft.com/7c2a8e24-0919-4fe6-9a31-a1d4b1d119ed">PIDListSpanningEvent</a> structure.</td>
</tr>
<tr>
<td>EVENTID_RRTSpanningEvent</td>
<td>Contains information about a rating region table (RRT). The data is a <a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION</a> structure.</td>
</tr>
<tr>
<td>EVENTID_SignalAndServiceStatusSpanningEvent</td>
<td>Signals the current state of the television service. The event data is a member of the <a href="https://msdn.microsoft.com/88da8346-661c-4638-809d-4ef01f191cbe">SignalAndServiceStatusSpanningEvent_State</a> enumeration.</td>
</tr>
<tr>
<td>EVENTID_StreamIDSpanningEvent</td>
<td>Contains a stream identifier descriptor.  The event data has the same format as the EVENTID_AudioDescriptorSpanningEvent event.</td>
</tr>
<tr>
<td>EVENTID_StreamTypeSpanningEvent</td>
<td>Specifies the stream type. The event data is a <b>DWORD</b> that contains a value from the <a href="https://msdn.microsoft.com/10df5a9e-965c-4118-8ece-2d8ee353cd10">MPEG2StreamType</a> enumeration.</td>
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




<a href="https://msdn.microsoft.com/155a2e61-3b53-4225-b298-ee51e2afca96">ISBE2SpanningEvent</a>



<a href="https://msdn.microsoft.com/f1fc2b7c-3f60-4d03-9c75-9b9d9450ceef">ISBE2SpanningEvent::GetEvent</a>
 

 

