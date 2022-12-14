---
UID: NN:segment.IMSVidAnalogTunerEvent
title: IMSVidAnalogTunerEvent (segment.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["IMSVidAnalogTunerEvent","IMSVidAnalogTunerEvent interface [Microsoft TV Technologies]","IMSVidAnalogTunerEvent interface [Microsoft TV Technologies]","described","IMSVidAnalogTunerEventInterface","mstv.imsvidanalogtunerevent","segment/IMSVidAnalogTunerEvent"]
old-location: mstv\imsvidanalogtunerevent.htm
tech.root: mstv
ms.assetid: bf1c6eb1-64c1-43cc-900c-306c01fec9cc
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTunerEvent, IMSVidAnalogTunerEvent interface [Microsoft TV Technologies], IMSVidAnalogTunerEvent interface [Microsoft TV Technologies],described, IMSVidAnalogTunerEventInterface, mstv.imsvidanalogtunerevent, segment/IMSVidAnalogTunerEvent
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
 - IMSVidAnalogTunerEvent
 - segment/IMSVidAnalogTunerEvent
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
 - IMSVidAnalogTunerEvent
---

# IMSVidAnalogTunerEvent interface


## -description

This topic applies to Windows XP or later.
        

The <b>IMSVidAnalogTunerEvent</b> interface is used to receive events from non-BDA analog tuners.

This interface is an outgoing connection-point interface. To receive events related to analog tuning, implement this interface in your application. Then call the <b>IConnectionPoint::Advise</b> method on the <a href="/previous-versions/windows/desktop/mstv/msvidanalogtunerdevice">MSVidAnalogTunerDevice</a> object to establish a connection.

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAnalogTunerEvent)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidtunerevent">IMSVidTunerEvent</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Event Interfaces</a>