---
UID: NN:segment.IMSVidStreamBufferSink3
title: IMSVidStreamBufferSink3
author: windows-driver-content
description: The IMSVidStreamBufferSink3 interface represents the Stream Buffer Sink filter within the Video Control.
old-location: mstv\imsvidstreambuffersink3.htm
old-project: mstv
ms.assetid: 5768936b-9c0a-4177-82da-cc6ebe62ea67
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferSink3, IMSVidStreamBufferSink3 interface [Microsoft TV Technologies], IMSVidStreamBufferSink3 interface [Microsoft TV Technologies], described, IMSVidStreamBufferSink3Interface, mstv.imsvidstreambuffersink3, segment/IMSVidStreamBufferSink3
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
-	IMSVidStreamBufferSink3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferSink3 interface


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        </div>
<div> </div>


The <b>IMSVidStreamBufferSink3</b> interface represents the Stream Buffer Sink filter within the Video Control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSink3</b> interface inherits from <a href="https://msdn.microsoft.com/d279378b-2309-4d46-8fef-a00b3121c6c7">IMSVidStreamBufferSink2</a>. <b>IMSVidStreamBufferSink3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSink3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a66ec9d3-f27b-45b5-b8f4-6779a5069cde">get__AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ca6bef1-807c-4dfb-bb9e-ef90af70e981">get__DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e782f4e-9f83-4899-b4b6-18c8dcb73211">get__VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46636a23-dc2a-4c75-ab10-101892b4a9c5">get_AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8947b90e-4fb6-419a-8207-fa86ec25d40c">get_AudioCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76c3e3e5-521a-40d3-98b9-c5a757fc2bec">get_CCCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the closed captioning stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/272861fa-61c2-466e-b65a-c63a1ae98929">get_DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f20b8845-86ae-4fe9-9d2b-80341672843c">get_LicenseErrorCode</a>
</td>
<td align="left" width="63%">
Returns the most recent error code relating to licenses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f4080d3-4092-4a36-9e2e-5a53bffe9ee3">get_VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0213f84b-7b82-4326-92c9-86459c8c60ba">get_VideoCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4698bcce-e3df-4631-a363-0b3d54f8e38a">get_WSTCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the World Standard Teletext (WST) stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c8cba5f-f060-441d-804d-7eb6bc95cb2b">put__AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0a5148d-68bb-44a3-b7b3-d278c177f746">put__DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77664778-5be3-45b7-9d33-37c923070080">put__VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73068ef6-ab3c-41a5-9624-441d764a3a3c">put_AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a353c20-7804-4277-a5cb-de0a7a610dc5">put_DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1ac3517-2f83-409c-b393-5bcbfff685c3">put_VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f7a7323-c9da-47f9-95e2-dd13fc023373">SetMinSeek</a>
</td>
<td align="left" width="63%">
Sets the minimum seek position equal to the current playback position, and retrieves the current position.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSink3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/d279378b-2309-4d46-8fef-a00b3121c6c7">IMSVidStreamBufferSink2</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

