---
UID: NN:segment.IMSVidVideoInputDevice
title: IMSVidVideoInputDevice (segment.h)
author: windows-sdk-content
description: The IMSVidVideoInputDevice interface represents a video input device. This interface inherits from the IMSVidInputDevice interface but adds no methods to it. It exists to support polymorphism.
old-location: mstv\imsvidvideoinputdevice.htm
tech.root: mstv
ms.assetid: cbc687b1-826d-4738-8d0a-a7b90f5ff20d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidVideoInputDevice, IMSVidVideoInputDevice interface [Microsoft TV Technologies], IMSVidVideoInputDevice interface [Microsoft TV Technologies],described, mstv.imsvidvideoinputdevice, segment/IMSVidVideoInputDevice
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoInputDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoInputDevice interface


## -description


The <b>IMSVidVideoInputDevice</b> interface represents a video input device. This interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice</a> interface but adds no methods to it. It exists to support polymorphism.

The <a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidtuner">IMSVidTuner</a> interface, which represents video tuning devices, inherits from this interface.


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoInputDevice)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

