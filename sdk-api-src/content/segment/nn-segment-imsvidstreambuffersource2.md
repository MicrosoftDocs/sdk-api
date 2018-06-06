---
UID: NN:segment.IMSVidStreamBufferSource2
title: IMSVidStreamBufferSource2
author: windows-sdk-content
description: The IMSVidStreamBufferSource2 interface represents the Stream Buffer Source filter within the Video Control.
old-location: mstv\imsvidstreambuffersource2.htm
old-project: mstv
ms.assetid: 47012868-4c9e-4974-8549-11331836bed0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidStreamBufferSource2, IMSVidStreamBufferSource2 interface [Microsoft TV Technologies], IMSVidStreamBufferSource2 interface [Microsoft TV Technologies],described, IMSVidStreamBufferSource2Interface, mstv.imsvidstreambuffersource2, segment/IMSVidStreamBufferSource2
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
 - IMSVidStreamBufferSource2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSource2 interface


## -description



<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>


The <b>IMSVidStreamBufferSource2</b> interface represents the Stream Buffer Source filter within the Video Control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSource2</b> interface inherits from <a href="https://msdn.microsoft.com/12160959-820b-4534-9392-a13ad229317d">IMSVidStreamBufferSource</a>. <b>IMSVidStreamBufferSource2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSource2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/310e59e1-afde-45ed-b2d1-eecf59319935">get_AudioCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58aa567a-6ef3-4e8b-9155-f262ac1a7557">get_CCCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the closed captioning stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9def9b51-bae7-49a2-b32f-61811be63c58">get_VideoCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a506a152-c0e7-497b-a494-5464f712f432">get_WSTCounter</a>
</td>
<td align="left" width="63%">
Enables the caller to get performance statistics from the Stream Buffer Source for the World Standard Teletext (WST) stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b213ad08-8a72-4b4a-bffa-b68783693340">put_RateEx</a>
</td>
<td align="left" width="63%">
Sets the playback rate, and sets the frame rate for fast-forward play ("trick mode").

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSource2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/12160959-820b-4534-9392-a13ad229317d">IMSVidStreamBufferSource</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

