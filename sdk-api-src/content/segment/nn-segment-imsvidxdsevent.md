---
UID: NN:segment.IMSVidXDSEvent
title: IMSVidXDSEvent (segment.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. The IMSVidXDSEvent interface is used to receive events from the MSVidXDS object.This interface is an outgoing connection-point interface.
helpviewer_keywords: ["IMSVidXDSEvent","IMSVidXDSEvent interface [Microsoft TV Technologies]","IMSVidXDSEvent interface [Microsoft TV Technologies]","described","IMSVidXDSEventInterface","mstv.imsvidxdsevent","segment/IMSVidXDSEvent"]
old-location: mstv\imsvidxdsevent.htm
tech.root: mstv
ms.assetid: c89f378d-daa6-4e01-a087-6082d368585b
ms.date: 12/05/2018
ms.keywords: IMSVidXDSEvent, IMSVidXDSEvent interface [Microsoft TV Technologies], IMSVidXDSEvent interface [Microsoft TV Technologies],described, IMSVidXDSEventInterface, mstv.imsvidxdsevent, segment/IMSVidXDSEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidXDSEvent
 - segment/IMSVidXDSEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidXDSEvent
---

# IMSVidXDSEvent interface


## -description

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>


The <b>IMSVidXDSEvent</b> interface is used to receive events from the <a href="/previous-versions/windows/desktop/legacy/dd695263(v=vs.85)">MSVidXDS</a> object.

This interface is an outgoing connection-point interface. To receive events from a playback device, implement this interface and then call the <b>IConnectionPoint::Advise</b> method to establish a connection.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidXDSEvent</b> interface inherits from <a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfeatureevent">IMSVidFeatureEvent</a>. <b>IMSVidXDSEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidXDSEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/segment/nf-segment-imsvidxdsevent-ratingchange">RatingChange</a>
</td>
<td align="left" width="63%">
Called when the current rating changes.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidXDSEvent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidfeatureevent">IMSVidFeatureEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>