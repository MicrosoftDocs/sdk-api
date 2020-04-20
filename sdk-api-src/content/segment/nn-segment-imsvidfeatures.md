---
UID: NN:segment.IMSVidFeatures
title: IMSVidFeatures (segment.h)
description: The IMSVidFeatures interface represents a collection of Video Control features.helpviewer_keywords: ["IMSVidFeatures","IMSVidFeatures interface [Microsoft TV Technologies]","IMSVidFeatures interface [Microsoft TV Technologies]","described","IMSVidFeaturesInterface","mstv.imsvidfeatures","segment/IMSVidFeatures"]
old-location: mstv\imsvidfeatures.htm
tech.root: mstv
ms.assetid: 19790fab-0530-4a17-8a3c-a50576fea9ca
ms.date: 12/05/2018
ms.keywords: IMSVidFeatures, IMSVidFeatures interface [Microsoft TV Technologies], IMSVidFeatures interface [Microsoft TV Technologies],described, IMSVidFeaturesInterface, mstv.imsvidfeatures, segment/IMSVidFeatures
f1_keywords:
- segment/IMSVidFeatures
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidFeatures interface


## -description



The <b>IMSVidFeatures</b> interface represents a collection of Video Control features. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695126(v=vs.85)">MSVidFeatures</a> collection object exposes this interface.

This interface is used for two purposes: to retrieve a read-only collection of the features available on the current system (the <i>available</i> features collection), and to create a read/write list of activated features (the <i>active</i> features collection).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidFeatures</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidFeatures</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-add">Add</a>
</td>
<td align="left" width="63%">
Adds a feature to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFeatures)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

