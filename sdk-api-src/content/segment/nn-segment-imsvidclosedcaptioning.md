---
UID: NN:segment.IMSVidClosedCaptioning
title: IMSVidClosedCaptioning (segment.h)
description: The IMSVidClosedCaptioning interface enables or disables closed captions.
helpviewer_keywords: ["IMSVidClosedCaptioning","IMSVidClosedCaptioning interface [Microsoft TV Technologies]","IMSVidClosedCaptioning interface [Microsoft TV Technologies]","described","IMSVidClosedCaptioningInterface","mstv.imsvidclosedcaptioning","segment/IMSVidClosedCaptioning"]
old-location: mstv\imsvidclosedcaptioning.htm
tech.root: mstv
ms.assetid: 070a208b-cf4c-41e1-9a5f-76cc444285c9
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning, IMSVidClosedCaptioning interface [Microsoft TV Technologies], IMSVidClosedCaptioning interface [Microsoft TV Technologies],described, IMSVidClosedCaptioningInterface, mstv.imsvidclosedcaptioning, segment/IMSVidClosedCaptioning
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
 - IMSVidClosedCaptioning
 - segment/IMSVidClosedCaptioning
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
 - IMSVidClosedCaptioning
---

# IMSVidClosedCaptioning interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidClosedCaptioning</b> interface enables or disables closed captions. The <a href="/previous-versions/windows/desktop/legacy/dd695119(v=vs.85)">MSVidClosedCaptioning</a> feature exposes this interface.

To obtain this interface, enumerate the collection of available features on the Video Control. To use closed captioning, activate the closed captioning feature before you build the graph. Once the feature is active, you can enable or disable the closed captioning display by calling the <a href="/windows/desktop/api/segment/nf-segment-imsvidclosedcaptioning-put_enable">IMSVidClosedCaptioning::put_Enable</a> method.

## -inheritance

The <b>IMSVidClosedCaptioning</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>. <b>IMSVidClosedCaptioning</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidClosedCaptioning)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/displaying-closed-captioning-in-c">Displaying Closed Captioning in C++</a>



<a href="/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
