---
UID: NN:segment.IMSVidStreamBufferSourceEvent3
title: IMSVidStreamBufferSourceEvent3 (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersourceevent3.htm
tech.root: mstv
ms.assetid: 4ff2e05f-1c26-48f2-8c46-beebb8b0b1b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent3, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEvent3Interface, mstv.imsvidstreambuffersourceevent3, segment/IMSVidStreamBufferSourceEvent3
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
 - IMSVidStreamBufferSourceEvent3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSourceEvent3 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSourceEvent3</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/4043e199-d329-45f3-80a7-cd84fad88979">MSVidStreamBufferSource</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSourceEvent3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd694670(v=VS.85).aspx">IMSVidStreamBufferSourceEvent2</a>. <b>IMSVidStreamBufferSourceEvent3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd694673(v=VS.85).aspx">BroadcastEvent</a>
</td>
<td align="left" width="63%">
Called when the object receives a broadcast event through the <a href="https://msdn.microsoft.com/90d4fbc7-d552-460b-96b2-77e2347af716">IBroadcastEvent</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694674(v=VS.85).aspx">BroadcastEventEx</a>
</td>
<td align="left" width="63%">
Called when the object receives a broadcast event through the <a href="https://msdn.microsoft.com/c16ad538-afc6-4530-a2fd-18965b63983b">IBroadcastEventEx</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694675(v=VS.85).aspx">ContentPrimarilyAudio</a>
</td>
<td align="left" width="63%">
Called when the Stream Buffer Engine is processing primarily audio data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694676(v=VS.85).aspx">COPPBlocked</a>
</td>
<td align="left" width="63%">
Called when the content is blocked because of the Certified Output Protection Protocol (COPP) status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694677(v=VS.85).aspx">COPPUnblocked</a>
</td>
<td align="left" width="63%">
Called when the content is unblocked after a <b>COPPBlocked</b> event.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694670(v=VS.85).aspx">IMSVidStreamBufferSourceEvent2</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

