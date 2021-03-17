---
UID: NN:segment.IMSVidOutputDevice
title: IMSVidOutputDevice (segment.h)
description: The IMSVidOutputDevice interface represents an output device. This interface derives from the IMSVidDevice interface but adds no methods to it. It exists to support polymorphism.
helpviewer_keywords: ["IMSVidOutputDevice","IMSVidOutputDevice interface [Microsoft TV Technologies]","IMSVidOutputDevice interface [Microsoft TV Technologies]","described","IMSVidOutputDeviceInterface","mstv.imsvidoutputdevice","segment/IMSVidOutputDevice"]
old-location: mstv\imsvidoutputdevice.htm
tech.root: mstv
ms.assetid: c2e5ebac-cb10-4567-83f7-f8f4e3b4f009
ms.date: 12/05/2018
ms.keywords: IMSVidOutputDevice, IMSVidOutputDevice interface [Microsoft TV Technologies], IMSVidOutputDevice interface [Microsoft TV Technologies],described, IMSVidOutputDeviceInterface, mstv.imsvidoutputdevice, segment/IMSVidOutputDevice
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
 - IMSVidOutputDevice
 - segment/IMSVidOutputDevice
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
 - IMSVidOutputDevice
---

# IMSVidOutputDevice interface


## -description

The <b>IMSVidOutputDevice</b> interface represents an output device. This interface derives from the <a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice</a> interface but adds no methods to it. It exists to support polymorphism.

Output devices include audio and video renderers, and the Stream Buffer Sink object. Video renderers expose the <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a> interface, and audio renderers exposes the <a href="/previous-versions/windows/desktop/mstv/msvidaudiorenderer">IMSVidAudioRenderer</a> interface, both of which derive from <b>IMSVidOutputDevice</b>.

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidOutputDevice)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsviddevice">IMSVidDevice</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>