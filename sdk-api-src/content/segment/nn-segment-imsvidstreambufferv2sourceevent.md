---
UID: NN:segment.IMSVidStreamBufferV2SourceEvent
title: IMSVidStreamBufferV2SourceEvent
author: windows-sdk-content
description: Implements an event system for the Stream Buffer Engine, version 2 (SBE2) source filter that is wrapped in the Video Control. Each event corresponds to an event that the SBE2 source filter receives inside a DirectShow graph.
old-location: mstv\imsvidstreambufferv2sourceevent.htm
old-project: mstv
ms.assetid: ab463f6e-0718-4420-89bc-28b3c447f3a0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidStreamBufferV2SourceEvent, IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies], IMSVidStreamBufferV2SourceEvent interface [Microsoft TV Technologies],described, mstv.imsvidstreambufferv2sourceevent, segment/IMSVidStreamBufferV2SourceEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferV2SourceEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/f5d5b6d8-9baa-4a9e-8275-e817394c211a">BroadcastEvent</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives any event through the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> interface, other than  the EVENTID_DTFilterRatingChange event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/731baecc-72f9-4ecd-bc01-40ad31c67051">BroadcastEventEx</a>
</td>
<td align="left" width="63%">

            Fired when an SBE2 source filter receives any event fired by a call to <a href="https://msdn.microsoft.com/b9ad8d9d-9827-44f9-9d2b-3f662c32eb9b">IBroadcastEventEx::FireEx</a>.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9af548a-9796-4dc0-8b78-46e529a484ce">ContentBecomingStale</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives a TREAMBUFFER_EC_CONTENT_BECOMING_STALE event, which indicates the stream buffer source lags behind the stream buffer sink by more than a preset number of files.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9056bed3-b4da-4eca-a573-0d9bda3d2127">ContentPrimarilyAudio</a>
</td>
<td align="left" width="63%">

            Fired when an SBE2 source filter receives a STREAMBUFFER_EC_PRIMARY_AUDIO event that was fired through the <a href="https://msdn.microsoft.com/4ff2e05f-1c26-48f2-8c46-beebb8b0b1b3">IMSVidStreamBufferSourceEvent3</a> interface and indicates SBE is processing primarily audio data.
          
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32af2323-0018-4e77-bf2e-9ff95e59f91e">RateChange</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives a STREAMBUFFER_EC_RATE_CHANGED event, which indicates the playback rate has changed.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56ba6126-c3c7-4cbd-9209-7638452d5782">RatingsChanged</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives an EVENTID_DTFilterRatingChange event that was fired through the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> interface and  indicates  a rating has changed.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eb53b77-94a3-4216-a32f-22338d84f5ad">StaleDataRead</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_DATA_READ event, which indicates an <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object has read from a temporary recording file that is marked for deletion.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23cd93d9-3615-4fbf-a6de-61ee69cd51e3">StaleFileDeleted</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives a STREAMBUFFER_EC_STALE_FILE_DELETED event, which indicates a temporary file has been deleted.
          
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eceda3b-b3d6-4714-85c5-ec8bb0986b6f">TimeHole</a>
</td>
<td align="left" width="63%">

            Fired when the SBE2 source filter receives a STREAMBUFFER_EC_TIMEHOLE event, which indicates playback has reached a gap in recorded content.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferV2SourceEvent)</code>.



