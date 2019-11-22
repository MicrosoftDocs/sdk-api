---
UID: NN:segment.IMSVidStreamBufferSourceEvent2
title: IMSVidStreamBufferSourceEvent2 (segment.h)

description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IMSVidStreamBufferSourceEvent2 interface is used to receive events from the MSVidStreamBufferSource object.
old-location: mstv\imsvidstreambuffersourceevent2.htm
tech.root: mstv
ms.assetid: d601efcf-d15a-4b9a-bad8-f09de80500c6

ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSourceEvent2, IMSVidStreamBufferSourceEvent2 interface [Microsoft TV Technologies], IMSVidStreamBufferSourceEvent2 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSourceEvent2Interface, mstv.imsvidstreambuffersourceevent2, segment/IMSVidStreamBufferSourceEvent2
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidStreamBufferSourceEvent2"
dev_langs:
 - c++
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
 - IMSVidStreamBufferSourceEvent2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSourceEvent2 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSourceEvent2</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695136(v=vs.85)">MSVidStreamBufferSource</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSourceEvent2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent</a>. <b>IMSVidStreamBufferSourceEvent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSourceEvent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent2-ratechange">RateChange</a>
</td>
<td align="left" width="63%">
Called when the playback rate changes.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSourceEvent2)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent">IMSVidStreamBufferSourceEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

