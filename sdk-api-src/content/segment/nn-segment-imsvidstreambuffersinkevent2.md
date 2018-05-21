---
UID: NN:segment.IMSVidStreamBufferSinkEvent2
title: IMSVidStreamBufferSinkEvent2
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IMSVidStreamBufferSinkEvent2 interface is used to receive events from the MSVidStreamBufferSink object.
old-location: mstv\imsvidstreambuffersinkevent2.htm
old-project: mstv
ms.assetid: 9e44b248-fc8a-44c1-9da6-8afb7649f6f4
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidStreamBufferSinkEvent2, IMSVidStreamBufferSinkEvent2 interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent2 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEvent2Interface, mstv.imsvidstreambuffersinkevent2, segment/IMSVidStreamBufferSinkEvent2
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
-	IMSVidStreamBufferSinkEvent2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferSinkEvent2 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSinkEvent2</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/87605ac5-a43b-45c5-9636-4e2d1dcf3f3f">MSVidStreamBufferSink</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent2</b> interface inherits from <a href="https://msdn.microsoft.com/e828d3e0-5a2a-499a-a718-11aa76a01b1b">IMSVidStreamBufferSinkEvent</a>. <b>IMSVidStreamBufferSinkEvent2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a4798851-b8e1-4b49-aba9-b8b06d91280d">EncryptionOff</a>
</td>
<td align="left" width="63%">
The stream is no longer encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/753f33bc-2430-4c76-bf9b-ccd5aeaf6676">EncryptionOn</a>
</td>
<td align="left" width="63%">
The stream is now encrypted

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/e828d3e0-5a2a-499a-a718-11aa76a01b1b">IMSVidStreamBufferSinkEvent</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

