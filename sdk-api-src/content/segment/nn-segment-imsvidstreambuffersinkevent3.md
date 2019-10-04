---
UID: NN:segment.IMSVidStreamBufferSinkEvent3
title: IMSVidStreamBufferSinkEvent3 (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersinkevent3.htm
tech.root: mstv
ms.assetid: 3d76be50-0e67-4e23-8ce0-8ac9f4ad0c1c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent3, IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEvent3Interface, mstv.imsvidstreambuffersinkevent3, segment/IMSVidStreamBufferSinkEvent3
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidStreamBufferSinkEvent3"
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
 - IMSVidStreamBufferSinkEvent3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSinkEvent3 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSinkEvent3</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695135(v=vs.85)">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent2">IMSVidStreamBufferSinkEvent2</a>. <b>IMSVidStreamBufferSinkEvent3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSinkEvent3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersinkevent3-licensechange">LicenseChange</a>
</td>
<td align="left" width="63%">
The license for the content has changed.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent3)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidstreambuffersinkevent2">IMSVidStreamBufferSinkEvent2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

