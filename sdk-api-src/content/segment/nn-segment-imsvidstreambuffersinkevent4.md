---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

