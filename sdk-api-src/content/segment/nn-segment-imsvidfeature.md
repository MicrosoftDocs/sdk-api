---
UID: NN:segment.IMSVidFeature
title: IMSVidFeature (segment.h)
description: The IMSVidFeature interface represents a feature that is available through the Video Control, such as data services or closed captioning.
helpviewer_keywords: ["IMSVidFeature","IMSVidFeature interface [Microsoft TV Technologies]","IMSVidFeature interface [Microsoft TV Technologies]","described","IMSVidFeatureInterface","mstv.imsvidfeature","segment/IMSVidFeature"]
old-location: mstv\imsvidfeature.htm
tech.root: mstv
ms.assetid: 0512e1d6-e10e-421e-846c-4bcd7e86d0e7
ms.date: 12/05/2018
ms.keywords: IMSVidFeature, IMSVidFeature interface [Microsoft TV Technologies], IMSVidFeature interface [Microsoft TV Technologies],described, IMSVidFeatureInterface, mstv.imsvidfeature, segment/IMSVidFeature
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
 - IMSVidFeature
 - segment/IMSVidFeature
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
 - IMSVidFeature
---

# IMSVidFeature interface


## -description

The <b>IMSVidFeature</b> interface represents a feature that is available through the Video Control, such as data services or closed captioning.

## -remarks

To obtain a collection of the features that are available, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_featuresavailable">IMSVidCtl::get_FeaturesAvailable</a> method on the Video Control. To activate a feature, create a new <a href="/previous-versions/windows/desktop/legacy/dd695126(v=vs.85)">MSVidFeatures</a> collection object and assign it to the Video Control by calling the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_featuresactive">IMSVidCtl::put_FeaturesActive</a> method.
      

Feature objects do not implement the <a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get_power">IMSVidDevice::get_Power</a> or <a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get_status">IMSVidDevice::get_Status</a> method.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFeature)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>