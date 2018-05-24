---
UID: NN:segment.IMSVidStreamBufferSinkEvent
title: IMSVidStreamBufferSinkEvent
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\imsvidstreambuffersinkevent.htm
old-project: mstv
ms.assetid: e828d3e0-5a2a-499a-a718-11aa76a01b1b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidStreamBufferSinkEvent, IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEventInterface, mstv.imsvidstreambuffersinkevent, segment/IMSVidStreamBufferSinkEvent
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSinkEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSinkEvent interface


## -description



This topic applies to Windows XP Service Pack 1 or later.
        

The <b>IMSVidStreamBufferSinkEvent</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/87605ac5-a43b-45c5-9636-4e2d1dcf3f3f">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent</b> interface inherits from <a href="https://msdn.microsoft.com/4f3ad7c0-02fd-4232-89f1-49517c23ee28">IMSVidOutputDeviceEvent</a>. <b>IMSVidStreamBufferSinkEvent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/95745e17-2bf9-49a9-bbbf-2deab3fa1c86">CertificateFailure</a>
</td>
<td align="left" width="63%">
The object failed to get an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23ac75ee-02ee-4159-b503-65604a6601cb">CertificateSuccess</a>
</td>
<td align="left" width="63%">
The object succeeded in getting an encryption/decryption license.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aec07e1-57b9-4350-a48f-762fcf370d6a">WriteFailure</a>
</td>
<td align="left" width="63%">
A write error occured in the Stream Buffer Sink filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent)</code>.




## -see-also




<a href="https://msdn.microsoft.com/4f3ad7c0-02fd-4232-89f1-49517c23ee28">IMSVidOutputDeviceEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

