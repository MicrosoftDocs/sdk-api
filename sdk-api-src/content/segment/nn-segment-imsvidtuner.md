---
UID: NN:segment.IMSVidTuner
title: IMSVidTuner (segment.h)
description: The IMSVidTuner interface manages tuning devices.
helpviewer_keywords: ["IMSVidTuner","IMSVidTuner interface [Microsoft TV Technologies]","IMSVidTuner interface [Microsoft TV Technologies]","described","IMSVidTunerInterface","mstv.imsvidtuner","segment/IMSVidTuner"]
old-location: mstv\imsvidtuner.htm
tech.root: mstv
ms.assetid: b11f3ac4-c351-4017-9801-98d8edec7449
ms.date: 12/05/2018
ms.keywords: IMSVidTuner, IMSVidTuner interface [Microsoft TV Technologies], IMSVidTuner interface [Microsoft TV Technologies],described, IMSVidTunerInterface, mstv.imsvidtuner, segment/IMSVidTuner
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
 - IMSVidTuner
 - segment/IMSVidTuner
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
 - IMSVidTuner
---

# IMSVidTuner interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidTuner</b> interface manages tuning devices. It is exposed by the <a href="/previous-versions/windows/desktop/mstv/msvidbdatunerdevice">MSVidBDATunerDevice</a> object, which represents Broadcast Driver Architecture (BDA)-compliant tuning devices. Non-BDA analog tuners expose the <a href="/windows/desktop/api/segment/nn-segment-imsvidanalogtuner">IMSVidAnalogTuner</a> interface, which inherits from this interface.

## -inheritance

The <b>IMSVidTuner</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/msvidvideoinputdevice">IMSVidVideoInputDevice</a>. <b>IMSVidTuner</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidTuner)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideoinputdevice">IMSVidVideoInputDevice</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
