---
UID: NN:segment.IMSVidStreamBufferSink3
title: IMSVidStreamBufferSink3 (segment.h)
author: windows-sdk-content
description: The IMSVidStreamBufferSink3 interface represents the Stream Buffer Sink filter within the Video Control.
old-location: mstv\imsvidstreambuffersink3.htm
tech.root: mstv
ms.assetid: 5768936b-9c0a-4177-82da-cc6ebe62ea67
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink3, IMSVidStreamBufferSink3 interface [Microsoft TV Technologies], IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSink3Interface, mstv.imsvidstreambuffersink3, segment/IMSVidStreamBufferSink3
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
 - IMSVidStreamBufferSink3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSink3 interface


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        </div>
<div> </div>


The <b>IMSVidStreamBufferSink3</b> interface represents the Stream Buffer Sink filter within the Video Control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSink3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd694625(v=VS.85).aspx">IMSVidStreamBufferSink2</a>. <b>IMSVidStreamBufferSink3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd694636(v=VS.85).aspx">get__AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694637(v=VS.85).aspx">get__DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694638(v=VS.85).aspx">get__VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694628(v=VS.85).aspx">get_AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694629(v=VS.85).aspx">get_AudioCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694630(v=VS.85).aspx">get_CCCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the closed captioning stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694631(v=VS.85).aspx">get_DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694632(v=VS.85).aspx">get_LicenseErrorCode</a>
</td>
<td align="left" width="63%">
Returns the most recent error code relating to licenses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694633(v=VS.85).aspx">get_VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694634(v=VS.85).aspx">get_VideoCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694635(v=VS.85).aspx">get_WSTCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Sink for the World Standard Teletext (WST) stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694642(v=VS.85).aspx">put__AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694643(v=VS.85).aspx">put__DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694644(v=VS.85).aspx">put__VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694639(v=VS.85).aspx">put_AudioAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694640(v=VS.85).aspx">put_DataAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694641(v=VS.85).aspx">put_VideoAnalysisFilter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694645(v=VS.85).aspx">SetMinSeek</a>
</td>
<td align="left" width="63%">
Sets the minimum seek position equal to the current playback position, and retrieves the current position.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSink3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694625(v=VS.85).aspx">IMSVidStreamBufferSink2</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

