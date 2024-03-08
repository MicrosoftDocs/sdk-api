---
UID: NN:segment.IMSVidTunerEvent
title: IMSVidTunerEvent (segment.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["IMSVidTunerEvent","IMSVidTunerEvent interface [Microsoft TV Technologies]","IMSVidTunerEvent interface [Microsoft TV Technologies]","described","IMSVidTunerEventInterface","mstv.imsvidtunerevent","segment/IMSVidTunerEvent"]
old-location: mstv\imsvidtunerevent.htm
tech.root: mstv
ms.assetid: cdffe6ca-00b0-4230-963d-b4409413e5f5
ms.date: 12/05/2018
ms.keywords: IMSVidTunerEvent, IMSVidTunerEvent interface [Microsoft TV Technologies], IMSVidTunerEvent interface [Microsoft TV Technologies],described, IMSVidTunerEventInterface, mstv.imsvidtunerevent, segment/IMSVidTunerEvent
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
 - IMSVidTunerEvent
 - segment/IMSVidTunerEvent
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
 - IMSVidTunerEvent
---

# IMSVidTunerEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP or later.
        

The <b>IMSVidTunerEvent</b> interface is used to receive events from BDA-compliant digital TV tuners.

This interface is an outgoing connection-point interface. To receive events from a BDA digital tuner, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="/previous-versions/windows/desktop/mstv/msvidbdatunerdevice">MSVidBDATunerDevice</a> object to establish a connection.

## -inheritance

The <b>IMSVidTunerEvent</b> interface inherits from <a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidinputdeviceevent">IMSVidInputDeviceEvent</a>. <b>IMSVidTunerEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidTunerEvent)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/segment/nn-segment-imsvidinputdeviceevent">IMSVidInputDeviceEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>
