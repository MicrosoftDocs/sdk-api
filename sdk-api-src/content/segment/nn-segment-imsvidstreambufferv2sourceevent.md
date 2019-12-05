---
UID: NN:segment.IMSVidStreamBufferV2SourceEvent
title: IMSVidStreamBufferV2SourceEvent (segment.h)
description: Implements an event system for the Stream Buffer Engine, version 2 (SBE2) source filter that is wrapped in the Video Control. Each event corresponds to an event that the SBE2 source filter receives inside a DirectShow graph.
old-location: mstv\imsvidstreambufferv2sourceevent.htm
tech.root: mstv
ms.assetid: ab463f6e-0718-4420-89bc-28b3c447f3a0
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies], IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],described, mstv.imsvidstreambufferv2sourceevent, segment/IMSVidStreamBufferV2SourceEvent
ms.topic: interface
f1_keywords:
- segment/IMSVidStreamBufferV2SourceEvent
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- segment.h
api_name:
- IMSVidStreamBufferV2SourceEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferV2SourceEvent interface


## -description


Implements an event system for the Stream Buffer Engine, version 2 (SBE2) source filter that is wrapped in the Video Control. Each event corresponds to an event that the SBE2 source filter receives inside a DirectShow graph. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferV2SourceEvent</b> interface inherits from <b>IMSVidFilePlaybackEvent</b>. <b>IMSVidStreamBufferV2SourceEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferV2SourceEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-broadcastevent">BroadcastEvent</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives any event through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcastevent">IBroadcastEvent</a> interface, other than  the EVENTID_DTFilterRatingChange event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-broadcasteventex">BroadcastEventEx</a>
</td>
<td align="left" width="63%">
Fired when an SBE2 source filter receives any event fired by a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ibroadcasteventex-fireex">IBroadcastEventEx::FireEx</a>.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-contentbecomingstale">ContentBecomingStale</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives a TREAMBUFFER_EC_CONTENT_BECOMING_STALE event, which indicates the stream buffer source lags behind the stream buffer sink by more than a preset number of files.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-contentprimarilyaudio">ContentPrimarilyAudio</a>
</td>
<td align="left" width="63%">
Fired when an SBE2 source filter receives a STREAMBUFFER_EC_PRIMARY_AUDIO event that was fired through the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent3">IMSVidStreamBufferSourceEvent3</a> interface and indicates SBE is processing primarily audio data.
          
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-ratechange">RateChange</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives a STREAMBUFFER_EC_RATE_CHANGED event, which indicates the playback rate has changed.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-ratingschanged">RatingsChanged</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives an EVENTID_DTFilterRatingChange event that was fired through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcastevent">IBroadcastEvent</a> interface and  indicates  a rating has changed.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-staledataread">StaleDataRead</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_DATA_READ event, which indicates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object has read from a temporary recording file that is marked for deletion.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-stalefiledeleted">StaleFileDeleted</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_FILE_DELETED event, which indicates a temporary file has been deleted.
          
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambufferv2sourceevent-timehole">TimeHole</a>
</td>
<td align="left" width="63%">
Fired when the SBE2 source filter receives a STREAMBUFFER_EC_TIMEHOLE event, which indicates playback has reached a gap in recorded content.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferV2SourceEvent)</code>.



