---
UID: NN:segment.IMSVidFeature
title: IMSVidFeature
author: windows-sdk-content
description: The IMSVidFeature interface represents a feature that is available through the Video Control, such as data services or closed captioning.
old-location: mstv\imsvidfeature.htm
tech.root: mstv
ms.assetid: 0512e1d6-e10e-421e-846c-4bcd7e86d0e7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidFeature, IMSVidFeature interface [Microsoft TV Technologies], IMSVidFeature interface [Microsoft TV Technologies],described, IMSVidFeatureInterface, mstv.imsvidfeature, segment/IMSVidFeature
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
 - IMSVidFeature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidFeature interface


## -description


The <b>IMSVidFeature</b> interface represents a feature that is available through the Video Control, such as data services or closed captioning.


## -remarks



To obtain a collection of the features that are available, call the <a href="https://msdn.microsoft.com/73da686c-0c25-4dfb-8a13-681f1dac6a4a">IMSVidCtl::get_FeaturesAvailable</a> method on the Video Control. To activate a feature, create a new <a href="https://msdn.microsoft.com/dd826afd-b6a1-449e-937b-8341506d3e1a">MSVidFeatures</a> collection object and assign it to the Video Control by calling the <a href="https://msdn.microsoft.com/293506fa-3208-468e-982a-3c1f8ce0269b">IMSVidCtl::put_FeaturesActive</a> method.
      

Feature objects do not implement the <a href="https://msdn.microsoft.com/3be4247b-43d4-4a32-8643-7eb2637aee6f">IMSVidDevice::get_Power</a> or <a href="https://msdn.microsoft.com/b11df7f3-d227-4c74-89a3-90716b3b3a12">IMSVidDevice::get_Status</a> method.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFeature)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5ec85d18-2fed-4fd0-ab94-72d1d4f3f7ef">IMSVidDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

