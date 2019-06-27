---
UID: NN:segment.IMSVidStreamBufferSinkEvent2
title: IMSVidStreamBufferSinkEvent2 (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IMSVidStreamBufferSinkEvent2 interface is used to receive events from the MSVidStreamBufferSink object.
old-location: mstv\imsvidstreambuffersinkevent2.htm
tech.root: mstv
ms.assetid: 9e44b248-fc8a-44c1-9da6-8afb7649f6f4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent2, IMSVidStreamBufferSinkEvent2 interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent2 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEvent2Interface, mstv.imsvidstreambuffersinkevent2, segment/IMSVidStreamBufferSinkEvent2
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidStreamBufferSinkEvent2"
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
 - IMSVidStreamBufferSinkEvent2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSinkEvent2 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSinkEvent2</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695135(v=vs.85)">MSVidStreamBufferSink</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent">IMSVidStreamBufferSinkEvent</a>. <b>IMSVidStreamBufferSinkEvent2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSinkEvent2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersinkevent2-encryptionoff">EncryptionOff</a>
</td>
<td align="left" width="63%">
The stream is no longer encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersinkevent2-encryptionon">EncryptionOn</a>
</td>
<td align="left" width="63%">
The stream is now encrypted

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent2)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent">IMSVidStreamBufferSinkEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

