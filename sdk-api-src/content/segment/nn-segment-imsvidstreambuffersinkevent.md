---
UID: NN:segment.IMSVidStreamBufferSinkEvent
title: IMSVidStreamBufferSinkEvent (segment.h)
description: This topic applies to Windows XP Service Pack 1 or later.helpviewer_keywords: ["IMSVidStreamBufferSinkEvent","IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies]","IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies]","described","IMSVidStreamBufferSinkEventInterface","mstv.imsvidstreambuffersinkevent","segment/IMSVidStreamBufferSinkEvent"]
old-location: mstv\imsvidstreambuffersinkevent.htm
tech.root: mstv
ms.assetid: e828d3e0-5a2a-499a-a718-11aa76a01b1b
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSinkEvent, IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEventInterface, mstv.imsvidstreambuffersinkevent, segment/IMSVidStreamBufferSinkEvent
f1_keywords:
- segment/IMSVidStreamBufferSinkEvent
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
- IMSVidStreamBufferSinkEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSinkEvent interface


## -description



This topic applies to Windows XP Service Pack 1 or later.
        

The <b>IMSVidStreamBufferSinkEvent</b> interface is used to receive events from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695135(v=vs.85)">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidoutputdeviceevent">IMSVidOutputDeviceEvent</a>. <b>IMSVidStreamBufferSinkEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSinkEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersinkevent-certificatefailure">CertificateFailure</a>
</td>
<td align="left" width="63%">
The object failed to get an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersinkevent-certificatesuccess">CertificateSuccess</a>
</td>
<td align="left" width="63%">
The object succeeded in getting an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidstreambuffersinkevent-writefailure">WriteFailure</a>
</td>
<td align="left" width="63%">
A write error occured in the Stream Buffer Sink filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/segment/nn-segment-imsvidoutputdeviceevent">IMSVidOutputDeviceEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
 

 

