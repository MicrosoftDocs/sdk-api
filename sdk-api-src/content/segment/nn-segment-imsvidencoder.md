---
UID: NN:segment.IMSVidEncoder
title: IMSVidEncoder (segment.h)
description: The IMSVidEncoder interface represents the MSVidEncoder feature object, which is required for stream buffer applications using the Video Control. For more information, see Using the Stream Buffer Engine with the Video Control.
helpviewer_keywords: ["IMSVidEncoder","IMSVidEncoder interface [Microsoft TV Technologies]","IMSVidEncoder interface [Microsoft TV Technologies]","described","IMSVidEncoderInterface","mstv.imsvidencoder","segment/IMSVidEncoder"]
old-location: mstv\imsvidencoder.htm
tech.root: mstv
ms.assetid: 37d03dff-ae40-4e7f-a66f-facd0c1f6eee
ms.date: 12/05/2018
ms.keywords: IMSVidEncoder, IMSVidEncoder interface [Microsoft TV Technologies], IMSVidEncoder interface [Microsoft TV Technologies],described, IMSVidEncoderInterface, mstv.imsvidencoder, segment/IMSVidEncoder
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidEncoder
 - segment/IMSVidEncoder
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
 - IMSVidEncoder
---

# IMSVidEncoder interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidEncoder</b> interface represents the <a href="/previous-versions/windows/desktop/legacy/dd695123(v=vs.85)">MSVidEncoder</a> feature object, which is required for stream buffer applications using the Video Control. For more information, see <a href="/previous-versions/windows/desktop/mstv/using-the-stream-buffer-engine-with-the-video-control">Using the Stream Buffer Engine with the Video Control</a>.

## -inheritance

The <b>IMSVidEncoder</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>. <b>IMSVidEncoder</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidEncoder)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
