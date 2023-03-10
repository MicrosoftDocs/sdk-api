---
UID: NN:segment.IMSVidFeatureEvent
title: IMSVidFeatureEvent (segment.h)
description: The IMSVidFeatureEvent interface is the base interface for events from Video Control feature objects.
helpviewer_keywords: ["IMSVidFeatureEvent","IMSVidFeatureEvent interface [Microsoft TV Technologies]","IMSVidFeatureEvent interface [Microsoft TV Technologies]","described","IMSVidFeatureEventInterface","mstv.imsvidfeatureevent","segment/IMSVidFeatureEvent"]
old-location: mstv\imsvidfeatureevent.htm
tech.root: mstv
ms.assetid: 821a5524-5811-417b-9604-0883315080eb
ms.date: 12/05/2018
ms.keywords: IMSVidFeatureEvent, IMSVidFeatureEvent interface [Microsoft TV Technologies], IMSVidFeatureEvent interface [Microsoft TV Technologies],described, IMSVidFeatureEventInterface, mstv.imsvidfeatureevent, segment/IMSVidFeatureEvent
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
 - IMSVidFeatureEvent
 - segment/IMSVidFeatureEvent
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
 - IMSVidFeatureEvent
---

# IMSVidFeatureEvent interface


## -description

<div class="alert"><b>Note</b>  This topic applies to Windows XP or later.
        </div>
<div> </div>


The <b>IMSVidFeatureEvent</b> interface is the base interface for events from Video Control feature objects. Do not implement this interface directly. Other event interfaces derive from this interface.

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFeatureEvent)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddeviceevent">IMSVidDeviceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>