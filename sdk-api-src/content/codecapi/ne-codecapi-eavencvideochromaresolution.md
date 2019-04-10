---
UID: NE:codecapi.eAVEncVideoChromaResolution
title: eAVEncVideoChromaResolution (codecapi.h)
author: windows-sdk-content
description: Specifies chroma resolution. This enumeration is used with the AVEncVideoInputChromaResolution and AVEncVideoOutputChromaResolution properties.
old-location: dshow\eavencvideochromaresolution.htm
tech.root: DirectShow
ms.assetid: 63ac09a9-23bb-4d82-9699-541552e1ec90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoChromaResolution, codecapi/eAVEncVideoChromaResolution_411, codecapi/eAVEncVideoChromaResolution_420, codecapi/eAVEncVideoChromaResolution_422, codecapi/eAVEncVideoChromaResolution_444, codecapi/eAVEncVideoChromaResolution_SameAsSource, dshow.eavencvideochromaresolution, eAVEncVideoChromaResolution, eAVEncVideoChromaResolution enumeration [DirectShow], eAVEncVideoChromaResolutionEnumeration, eAVEncVideoChromaResolution_411, eAVEncVideoChromaResolution_420, eAVEncVideoChromaResolution_422, eAVEncVideoChromaResolution_444, eAVEncVideoChromaResolution_SameAsSource
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
 - eAVEncVideoChromaResolution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncVideoChromaResolution enumeration


## -description



Specifies chroma resolution. This enumeration is used with the <a href="https://msdn.microsoft.com/1e405def-2958-4f4f-9c15-db186e0df52f">AVEncVideoInputChromaResolution</a> and <a href="https://msdn.microsoft.com/b0614cdb-1eef-486d-85c1-d5644853fa94">AVEncVideoOutputChromaResolution</a> properties.




## -enum-fields




### -field eAVEncVideoChromaResolution_SameAsSource

Use the same chroma resolution as the input video. This flag applies to the <b>AVEncVideoOutputChromaResolution</b> property only.


### -field eAVEncVideoChromaResolution_444

4:4:4 (no downsampling).


### -field eAVEncVideoChromaResolution_422

4:2:2 (2:1 horizontal downsampling, with no vertical downsampling).


### -field eAVEncVideoChromaResolution_420

4:2:0 (2:1 horizontal downsampling, with 2:1 vertical downsampling).


### -field eAVEncVideoChromaResolution_411

4:1:1 (4:1 horizontal downsampling, with no vertical downsampling).


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

