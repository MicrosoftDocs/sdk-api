---
UID: NN:segment.IMSVidFeatures
title: IMSVidFeatures (segment.h)
description: The IMSVidFeatures interface represents a collection of Video Control features.
helpviewer_keywords: ["IMSVidFeatures","IMSVidFeatures interface [Microsoft TV Technologies]","IMSVidFeatures interface [Microsoft TV Technologies]","described","IMSVidFeaturesInterface","mstv.imsvidfeatures","segment/IMSVidFeatures"]
old-location: mstv\imsvidfeatures.htm
tech.root: mstv
ms.assetid: 19790fab-0530-4a17-8a3c-a50576fea9ca
ms.date: 12/05/2018
ms.keywords: IMSVidFeatures, IMSVidFeatures interface [Microsoft TV Technologies], IMSVidFeatures interface [Microsoft TV Technologies],described, IMSVidFeaturesInterface, mstv.imsvidfeatures, segment/IMSVidFeatures
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
 - IMSVidFeatures
 - segment/IMSVidFeatures
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
 - IMSVidFeatures
---

# IMSVidFeatures interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidFeatures</b> interface represents a collection of Video Control features. The <a href="/previous-versions/windows/desktop/legacy/dd695126(v=vs.85)">MSVidFeatures</a> collection object exposes this interface.

This interface is used for two purposes: to retrieve a read-only collection of the features available on the current system (the <i>available</i> features collection), and to create a read/write list of activated features (the <i>active</i> features collection).

## -inheritance

The <b>IMSVidFeatures</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidFeatures</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFeatures)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
