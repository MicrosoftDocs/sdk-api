---
UID: NN:segment.IMSVidFeatures
title: IMSVidFeatures
author: windows-sdk-content
description: The IMSVidFeatures interface represents a collection of Video Control features.
old-location: mstv\imsvidfeatures.htm
tech.root: MSTV
ms.assetid: 19790fab-0530-4a17-8a3c-a50576fea9ca
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidFeatures, IMSVidFeatures interface [Microsoft TV Technologies], IMSVidFeatures interface [Microsoft TV Technologies],described, IMSVidFeaturesInterface, mstv.imsvidfeatures, segment/IMSVidFeatures
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMSVidFeatures
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidFeatures interface


## -description



The <b>IMSVidFeatures</b> interface represents a collection of Video Control features. The <a href="https://msdn.microsoft.com/dd826afd-b6a1-449e-937b-8341506d3e1a">MSVidFeatures</a> collection object exposes this interface.

This interface is used for two purposes: to retrieve a read-only collection of the features available on the current system (the <i>available</i> features collection), and to create a read/write list of activated features (the <i>active</i> features collection).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidFeatures</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMSVidFeatures</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidFeatures</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bdb5e4a-4dd7-49dc-bb9c-b6a9e435219b">Add</a>
</td>
<td align="left" width="63%">
Adds a feature to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c619f62-5041-410b-8ce0-d811992a32d6">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45ad322a-d9ec-446d-8c1e-c955049dd257">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5656ba2-7ba6-44ba-bcab-3678fbd10b07">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a9e35e2-231e-4ad6-ac57-e6258df2777f">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFeatures)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

