---
UID: NN:segment.IMSVidStreamBufferSource
title: IMSVidStreamBufferSource
author: windows-driver-content
description: The IMSVidStreamBufferSource interface represents the Stream Buffer Source filter within the Video Control.
old-location: mstv\imsvidstreambuffersource.htm
old-project: mstv
ms.assetid: 12160959-820b-4534-9392-a13ad229317d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidStreamBufferSource, IMSVidStreamBufferSource interface [Microsoft TV Technologies], IMSVidStreamBufferSource interface [Microsoft TV Technologies], described, IMSVidStreamBufferSourceInterface, mstv.imsvidstreambuffersource, segment/IMSVidStreamBufferSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidStreamBufferSource interface


## -description



The <b>IMSVidStreamBufferSource</b> interface represents the Stream Buffer Source filter within the Video Control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSource</b> interface inherits from <a href="https://msdn.microsoft.com/d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5">IMSVidFilePlayback</a>. <b>IMSVidStreamBufferSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c388d972-07d9-4347-97d3-03a46a6bb50c">CurrentRatings</a>
</td>
<td align="left" width="63%">
Retrieves the current ratings information from the data source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e7020c8-778d-4a24-ae29-3e66d4ac165a">get_RecordingAttribute</a>
</td>
<td align="left" width="63%">
Retrieves the Stream Buffer Source filter that this object manages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ba9cf64-bf26-4a17-ae7a-3e92fc67138d">get_SBESource</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the Stream Buffer Source filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c6ad8b7-93d9-46de-b84a-a4575f3e6183">get_Start</a>
</td>
<td align="left" width="63%">
Retrieves the start time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74dbb008-21c9-4651-8386-761626b7bf19">MaxRatingsLevel</a>
</td>
<td align="left" width="63%">
Specifies the maximum ratings level the object is permitted to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dd59b87-708b-4003-9575-54a02b97c272">put_BlockUnrated</a>
</td>
<td align="left" width="63%">
Specifies whether to block unrated content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b4e1ac4-dfb8-45c0-9079-16f8babcb494">put_UnratedDelay</a>
</td>
<td align="left" width="63%">
Specifies the amount of time to play unrated content before blocking it.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSource)</code>.




## -see-also




<a href="https://msdn.microsoft.com/d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5">IMSVidFilePlayback</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

