---
UID: NN:segment.IMSVidStreamBufferSourceEvent
title: IMSVidStreamBufferSourceEvent (segment.h)
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersourceevent.htm
tech.root: mstv
ms.assetid: 6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent, IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEventInterface, mstv.imsvidstreambuffersourceevent, segment/IMSVidStreamBufferSourceEvent
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidStreamBufferSourceEvent"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSourceEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSourceEvent interface


## -description



This topic applies to Windows XP Service Pack 1 or later.
        

The <b>IMSVidStreamBufferSourceEvent</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSourceEvent</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfileplaybackevent">IMSVidFilePlaybackEvent</a>. <b>IMSVidStreamBufferSourceEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSourceEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-certificatefailure">CertificateFailure</a>
</td>
<td align="left" width="63%">
The object failed to get an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-certificatesuccess">CertificateSuccess</a>
</td>
<td align="left" width="63%">
The object succeeded in getting an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-contentbecomingstale">ContentBecomingStale</a>
</td>
<td align="left" width="63%">
Called when the stream buffer source lags behind the stream buffer sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-ratingsblocked">RatingsBlocked</a>
</td>
<td align="left" width="63%">
The object has blocked the stream, because the rating is not allowed under the current permissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-ratingschanged">RatingsChanged</a>
</td>
<td align="left" width="63%">
The current rating has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-ratingsunblocked">RatingsUnblocked</a>
</td>
<td align="left" width="63%">
The object has unblocked the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-staledataread">StaleDataRead</a>
</td>
<td align="left" width="63%">
Called when the <b>MSVidStreamBufferSource</b> object reads from a temporary recording file that has been marked for deletion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-stalefiledeleted">StaleFileDeleted</a>
</td>
<td align="left" width="63%">
Called when a temporary recording file is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent-timehole">TimeHole</a>
</td>
<td align="left" width="63%">
Called when playback reaches a gap in the recorded content.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfileplaybackevent">IMSVidFilePlaybackEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

