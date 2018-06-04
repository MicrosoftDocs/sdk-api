---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# eAVEncVideoColorNominalRange enumeration


## -description



Specifies the nominal range for a video source. This enumeration is used with the <a href="https://msdn.microsoft.com/e9f8fef5-73da-424d-a239-09779b81a02b">AVEncVideoInputChromaSubsampling</a> and <a href="https://msdn.microsoft.com/05acb05f-37e1-4953-bd24-ae790d355bf9">AVEncVideoOutputChromaSubsampling</a> properties.



The nominal range describes how luma components normalized to a range of [0..1] map to 8-bit or 10-bit samples. The mapping determines whether the color data includes headroom and toeroom. Headroom allows for values beyond 1.0 white ("whiter than white"), and toeroom allows for values below reference 0.0 black ("blacker than black").


## -enum-fields




### -field eAVEncVideoColorNominalRange_SameAsSource

Use the same nominal range as the input video. This flag applies to the <b>AVEncVideoOutputChromaSubsampling</b> property only.


### -field eAVEncVideoColorNominalRange_0_255

The normalized range [0..1] maps to [0...255] for 8-bit samples, or [0..1023] for 10-bit samples.


### -field eAVEncVideoColorNominalRange_16_235

The normalized range [0..1] maps to [16...235] for 8-bit samples, or [64..940] for 10-bit samples.


### -field eAVEncVideoColorNominalRange_48_208

The normalized range [0..1] maps to [48...208] for 8-bit samples.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

