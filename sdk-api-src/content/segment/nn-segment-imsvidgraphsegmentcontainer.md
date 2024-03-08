---
UID: NN:segment.IMSVidGraphSegmentContainer
title: IMSVidGraphSegmentContainer (segment.h)
description: The IMSVidGraphSegmentContainer interface is exposed by the Video Control and contains one supported method, get_Graph, which obtains a pointer to the Filter Graph Manager.
helpviewer_keywords: ["IMSVidGraphSegmentContainer","IMSVidGraphSegmentContainer interface [Microsoft TV Technologies]","IMSVidGraphSegmentContainer interface [Microsoft TV Technologies]","described","IMSVidGraphSegmentContainerInterface","mstv.imsvidgraphsegmentcontainer","segment/IMSVidGraphSegmentContainer"]
old-location: mstv\imsvidgraphsegmentcontainer.htm
tech.root: mstv
ms.assetid: a314693f-8fc2-4816-b64b-d5f8886da39e
ms.date: 12/05/2018
ms.keywords: IMSVidGraphSegmentContainer, IMSVidGraphSegmentContainer interface [Microsoft TV Technologies], IMSVidGraphSegmentContainer interface [Microsoft TV Technologies],described, IMSVidGraphSegmentContainerInterface, mstv.imsvidgraphsegmentcontainer, segment/IMSVidGraphSegmentContainer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidGraphSegmentContainer
 - segment/IMSVidGraphSegmentContainer
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
 - IMSVidGraphSegmentContainer
---

# IMSVidGraphSegmentContainer interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidGraphSegmentContainer</b> interface is exposed by the Video Control and contains one supported method, <a href="/windows/desktop/api/segment/nf-segment-imsvidgraphsegmentcontainer-get_graph">get_Graph</a>, which obtains a pointer to the Filter Graph Manager.

## -inheritance

The <b>IMSVidGraphSegmentContainer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMSVidGraphSegmentContainer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

This interface has additional methods besides the one shown here, but they are not supported.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidGraphSegmentContainer)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
