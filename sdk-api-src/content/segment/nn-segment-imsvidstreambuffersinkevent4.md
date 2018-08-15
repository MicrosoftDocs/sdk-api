---
UID: NN:segment.IMSVidStreamBufferSinkEvent4
title: IMSVidStreamBufferSinkEvent4
author: windows-sdk-content
description: The IMSVidStreamBufferSinkEvent4 interface receives events from the MSVidStreamBufferSink object.
old-location: mstv\imsvidstreambuffersinkevent4.htm
old-project: mstv
ms.assetid: afec7f7a-0c5b-47ca-b442-5dbdba54a7af
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidStreamBufferSinkEvent4, IMSVidStreamBufferSinkEvent4 interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent4 interface [Microsoft TV Technologies],described, mstv.imsvidstreambuffersinkevent4, segment/IMSVidStreamBufferSinkEvent4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSinkEvent4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidStreamBufferSinkEvent4 interface


## -description


The <a href="https://msdn.microsoft.com/e828d3e0-5a2a-499a-a718-11aa76a01b1b">IMSVidStreamBufferSinkEvent4</a> interface receives events from the <a href="https://msdn.microsoft.com/87605ac5-a43b-45c5-9636-4e2d1dcf3f3f">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent4</b> interface inherits from <a href="https://msdn.microsoft.com/3d76be50-0e67-4e23-8ce0-8ac9f4ad0c1c">IMSVidStreamBufferSinkEvent3</a>. <b>IMSVidStreamBufferSinkEvent4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSinkEvent4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5968d45-5fd2-460a-bbd8-38671bb98a14">WriteFailureClear</a>
</td>
<td align="left" width="63%">
A write error on the <a href="https://msdn.microsoft.com/1606eab6-84dc-49ba-8fb6-df3b8615bf85">Stream Buffer Sink</a> filter has been cleared.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent4)</code>.




## -see-also




<a href="https://msdn.microsoft.com/3d76be50-0e67-4e23-8ce0-8ac9f4ad0c1c">IMSVidStreamBufferSinkEvent3</a>



<a href="https://msdn.microsoft.com/87605ac5-a43b-45c5-9636-4e2d1dcf3f3f">MSVidStreamBufferSink</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

