---
UID: NN:segment.IMSVidOutputDevice
title: IMSVidOutputDevice
author: windows-sdk-content
description: The IMSVidOutputDevice interface represents an output device. This interface derives from the IMSVidDevice interface but adds no methods to it. It exists to support polymorphism.
old-location: mstv\imsvidoutputdevice.htm
tech.root: mstv
ms.assetid: c2e5ebac-cb10-4567-83f7-f8f4e3b4f009
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidOutputDevice, IMSVidOutputDevice interface [Microsoft TV Technologies], IMSVidOutputDevice interface [Microsoft TV Technologies],described, IMSVidOutputDeviceInterface, mstv.imsvidoutputdevice, segment/IMSVidOutputDevice
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMSVidOutputDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidOutputDevice interface


## -description


The <b>IMSVidOutputDevice</b> interface represents an output device. This interface derives from the <a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice</a> interface but adds no methods to it. It exists to support polymorphism.

Output devices include audio and video renderers, and the Stream Buffer Sink object. Video renderers expose the <a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer</a> interface, and audio renderers exposes the <a href="https://msdn.microsoft.com/f822b5a6-c88e-48c9-91f4-611a3f147fe0">IMSVidAudioRenderer</a> interface, both of which derive from <b>IMSVidOutputDevice</b>.


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidOutputDevice)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

