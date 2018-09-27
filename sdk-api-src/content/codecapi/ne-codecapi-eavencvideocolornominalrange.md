---
UID: NE:codecapi.eAVEncVideoColorNominalRange
title: eAVEncVideoColorNominalRange
author: windows-sdk-content
description: Specifies the nominal range for a video source. This enumeration is used with the AVEncVideoInputChromaSubsampling and AVEncVideoOutputChromaSubsampling properties.
old-location: dshow\eavencvideocolornominalrange.htm
tech.root: DirectShow
ms.assetid: e3f49d42-b683-463b-8e09-9497a9bfad25
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: codecapi/eAVEncVideoColorNominalRange, codecapi/eAVEncVideoColorNominalRange_0_255, codecapi/eAVEncVideoColorNominalRange_16_235, codecapi/eAVEncVideoColorNominalRange_48_208, codecapi/eAVEncVideoColorNominalRange_SameAsSource, dshow.eavencvideocolornominalrange, eAVEncVideoColorNominalRange, eAVEncVideoColorNominalRange enumeration [DirectShow], eAVEncVideoColorNominalRangeEnumeration, eAVEncVideoColorNominalRange_0_255, eAVEncVideoColorNominalRange_16_235, eAVEncVideoColorNominalRange_48_208, eAVEncVideoColorNominalRange_SameAsSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorNominalRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd387884(v=VS.85).aspx">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

