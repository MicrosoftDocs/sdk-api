---
UID: NN:segment.IMSVidStreamBufferSourceEvent3
title: IMSVidStreamBufferSourceEvent3 (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSourceEvent3","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSourceEvent3Interface","mstv.imsvidstreambuffersourceevent3","segment/IMSVidStreamBufferSourceEvent3"]
old-location: mstv\imsvidstreambuffersourceevent3.htm
tech.root: mstv
ms.assetid: 4ff2e05f-1c26-48f2-8c46-beebb8b0b1b3
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent3, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEvent3Interface, mstv.imsvidstreambuffersourceevent3, segment/IMSVidStreamBufferSourceEvent3
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSourceEvent3
 - segment/IMSVidStreamBufferSourceEvent3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSourceEvent3
---

# IMSVidStreamBufferSourceEvent3 interface


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSourceEvent3</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSourceEvent3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent2">IMSVidStreamBufferSourceEvent2</a>. <b>IMSVidStreamBufferSourceEvent3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSourceEvent3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent3-broadcastevent">BroadcastEvent</a>
</td>
<td align="left" width="63%">
Called when the object receives a broadcast event through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcastevent">IBroadcastEvent</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent3-broadcasteventex">BroadcastEventEx</a>
</td>
<td align="left" width="63%">
Called when the object receives a broadcast event through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ibroadcasteventex">IBroadcastEventEx</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent3-contentprimarilyaudio">ContentPrimarilyAudio</a>
</td>
<td align="left" width="63%">
Called when the Stream Buffer Engine is processing primarily audio data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent3-coppblocked">COPPBlocked</a>
</td>
<td align="left" width="63%">
Called when the content is blocked because of the Certified Output Protection Protocol (COPP) status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent3-coppunblocked">COPPUnblocked</a>
</td>
<td align="left" width="63%">
Called when the content is unblocked after a <b>COPPBlocked</b> event.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent3)</code>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent2">IMSVidStreamBufferSourceEvent2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>

