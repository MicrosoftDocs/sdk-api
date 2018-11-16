---
UID: NN:segment.IMSVidStreamBufferSourceEvent
title: IMSVidStreamBufferSourceEvent
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersourceevent.htm
tech.root: mstv
ms.assetid: 6d8e0cf3-b4c7-4f3e-acff-50f12b8340a8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidStreamBufferSourceEvent, IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEventInterface, mstv.imsvidstreambuffersourceevent, segment/IMSVidStreamBufferSourceEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSourceEvent interface


## -description



This topic applies to Windows XP Service Pack 1 or later.
        

The <b>IMSVidStreamBufferSourceEvent</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSourceEvent</b> interface inherits from <a href="https://msdn.microsoft.com/7dd435a1-8cd4-45c5-8250-770b629d3f3b">IMSVidFilePlaybackEvent</a>. <b>IMSVidStreamBufferSourceEvent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/10621576-65d0-46c1-8817-a96ee3822518">CertificateFailure</a>
</td>
<td align="left" width="63%">
The object failed to get an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c541058-5e02-4b78-8c28-a2a0709d5872">CertificateSuccess</a>
</td>
<td align="left" width="63%">
The object succeeded in getting an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff28174c-a5a7-4cd3-b967-3e52d53864f3">ContentBecomingStale</a>
</td>
<td align="left" width="63%">
Called when the stream buffer source lags behind the stream buffer sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d5e510e-9629-4249-a704-b7a995d27edf">RatingsBlocked</a>
</td>
<td align="left" width="63%">
The object has blocked the stream, because the rating is not allowed under the current permissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0754fb90-3f68-4f10-ab9b-74f7f7aeb047">RatingsChanged</a>
</td>
<td align="left" width="63%">
The current rating has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a255df5b-f7fe-4f99-9d29-59e30b922975">RatingsUnblocked</a>
</td>
<td align="left" width="63%">
The object has unblocked the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad8da4d8-9c8c-40e6-9fd4-a32cf8e775ce">StaleDataRead</a>
</td>
<td align="left" width="63%">
Called when the <b>MSVidStreamBufferSource</b> object reads from a temporary recording file that has been marked for deletion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/400efb81-6e16-4065-a9d8-3f0a801f306e">StaleFileDeleted</a>
</td>
<td align="left" width="63%">
Called when a temporary recording file is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f1c3d20-7ae2-4223-8481-c22ef8422531">TimeHole</a>
</td>
<td align="left" width="63%">
Called when playback reaches a gap in the recorded content.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/7dd435a1-8cd4-45c5-8250-770b629d3f3b">IMSVidFilePlaybackEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

