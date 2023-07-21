---
UID: NN:segment.IMSVidAnalogTuner
title: IMSVidAnalogTuner (segment.h)
description: The IMSVidAnalogTuner interface represents an analog-only tuner card that does not support the Broadcast Driver Architecture (BDA). This interface provides Automation access to the IAMTVTuner and IAMTVAudio interfaces.
helpviewer_keywords: ["IMSVidAnalogTuner","IMSVidAnalogTuner interface [Microsoft TV Technologies]","IMSVidAnalogTuner interface [Microsoft TV Technologies]","described","IMSVidAnalogTunerInterface","mstv.imsvidanalogtuner","segment/IMSVidAnalogTuner"]
old-location: mstv\imsvidanalogtuner.htm
tech.root: mstv
ms.assetid: 640143d3-6712-4e92-a1d9-0689637b3d90
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner, IMSVidAnalogTuner interface [Microsoft TV Technologies], IMSVidAnalogTuner interface [Microsoft TV Technologies],described, IMSVidAnalogTunerInterface, mstv.imsvidanalogtuner, segment/IMSVidAnalogTuner
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
 - IMSVidAnalogTuner
 - segment/IMSVidAnalogTuner
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
 - IMSVidAnalogTuner
---

# IMSVidAnalogTuner interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidAnalogTuner</b> interface represents an analog-only tuner card that does not support the Broadcast Driver Architecture (BDA). This interface provides Automation access to the <a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner</a> and <a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio</a> interfaces.

## -inheritance

The <b>IMSVidAnalogTuner</b> interface inherits from <a href="/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner</a>. <b>IMSVidAnalogTuner</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAnalogTuner)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
