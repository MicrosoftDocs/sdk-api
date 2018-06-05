---
UID: NN:segment.IMSVidGraphSegmentContainer
title: IMSVidGraphSegmentContainer
author: windows-sdk-content
description: The IMSVidGraphSegmentContainer interface is exposed by the Video Control and contains one supported method, get_Graph, which obtains a pointer to the Filter Graph Manager.
old-location: mstv\imsvidgraphsegmentcontainer.htm
old-project: mstv
ms.assetid: a314693f-8fc2-4816-b64b-d5f8886da39e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidGraphSegmentContainer, IMSVidGraphSegmentContainer interface [Microsoft TV Technologies], IMSVidGraphSegmentContainer interface [Microsoft TV Technologies],described, IMSVidGraphSegmentContainerInterface, mstv.imsvidgraphsegmentcontainer, segment/IMSVidGraphSegmentContainer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidGraphSegmentContainer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidGraphSegmentContainer interface


## -description



The <b>IMSVidGraphSegmentContainer</b> interface is exposed by the Video Control and contains one supported method, <a href="https://msdn.microsoft.com/fecc2953-84d6-4d1b-bb3f-5b966debef1e">get_Graph</a>, which obtains a pointer to the Filter Graph Manager. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidGraphSegmentContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMSVidGraphSegmentContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidGraphSegmentContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fecc2953-84d6-4d1b-bb3f-5b966debef1e">get_Graph</a>
</td>
<td align="left" width="63%">
Returns a pointer to the Filter Graph Manager.

</td>
</tr>
</table> 


## -remarks



This interface has additional methods besides the one shown here, but they are not supported.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGraphSegmentContainer)</code>.




## -see-also




<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

