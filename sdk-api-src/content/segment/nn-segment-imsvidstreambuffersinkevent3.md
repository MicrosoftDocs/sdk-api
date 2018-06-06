---
UID: NN:segment.IMSVidStreamBufferSinkEvent3
title: IMSVidStreamBufferSinkEvent3
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidstreambuffersinkevent3.htm
old-project: mstv
ms.assetid: 3d76be50-0e67-4e23-8ce0-8ac9f4ad0c1c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidStreamBufferSinkEvent3, IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies], IMSVidStreamBufferSinkEvent3 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkEvent3Interface, mstv.imsvidstreambuffersinkevent3, segment/IMSVidStreamBufferSinkEvent3
ms.prod: windows
ms.technology: windows-sdk
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
 - IMSVidStreamBufferSinkEvent3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSinkEvent3 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidStreamBufferSinkEvent3</b> interface is used to receive events from the <a href="https://msdn.microsoft.com/87605ac5-a43b-45c5-9636-4e2d1dcf3f3f">MSVidStreamBufferSink</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSinkEvent3</b> interface inherits from <a href="https://msdn.microsoft.com/9e44b248-fc8a-44c1-9da6-8afb7649f6f4">IMSVidStreamBufferSinkEvent2</a>. <b>IMSVidStreamBufferSinkEvent3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2477f082-50a6-4b4b-89ba-ccf4c8894a4b">LicenseChange</a>
</td>
<td align="left" width="63%">
The license for the content has changed.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSinkEvent3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/9e44b248-fc8a-44c1-9da6-8afb7649f6f4">IMSVidStreamBufferSinkEvent2</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Event Interfaces</a>
 

 

