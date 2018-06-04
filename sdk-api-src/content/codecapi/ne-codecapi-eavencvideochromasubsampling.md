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

# eAVEncVideoChromaSubsampling enumeration


## -description



Specifies chroma siting. Chroma siting defines the positions of the chroma samples relative to the luma samples. This enumeration is used with the <a href="https://msdn.microsoft.com/e9f8fef5-73da-424d-a239-09779b81a02b">AVEncVideoInputChromaSubsampling</a> and <a href="https://msdn.microsoft.com/05acb05f-37e1-4953-bd24-ae790d355bf9">AVEncVideoOutputChromaSubsampling</a> properties.




## -enum-fields




### -field eAVEncVideoChromaSubsamplingFormat_SameAsSource

Use the same chroma siting as the input video. This flag applies to the <b>AVEncVideoOutputChromaResolution</b> property only. This flag may not be combined with other flags.


### -field eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma

Chroma should be reconstructed as if the underlying video was progressive content, rather than skipping fields or applying chroma filtering to minimize artifacts from reconstructing 4:2:0 interlaced chroma.


### -field eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited

Chroma samples are aligned horizontally with multiples of the luma samples.


### -field eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited

Chroma samples are aligned vertically with multiples of the luma samples.


### -field eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes

The chroma planes have the same phase alignment. It is not valid to omit this flag unless the data is vertically cosited. If the data is not vertically cosited, this flag is required. If this flag is absent, the Cb and Cr samples are sited on alternate lines. For example, interlaced PAL DV video uses non-aligned chroma planes.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

