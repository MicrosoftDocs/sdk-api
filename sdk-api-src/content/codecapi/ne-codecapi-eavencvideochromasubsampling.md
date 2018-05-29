---
UID: NE:codecapi.eAVEncVideoChromaSubsampling
title: eAVEncVideoChromaSubsampling
author: windows-sdk-content
description: Specifies chroma siting. Chroma siting defines the positions of the chroma samples relative to the luma samples. This enumeration is used with the AVEncVideoInputChromaSubsampling and AVEncVideoOutputChromaSubsampling properties.
old-location: dshow\eavencvideochromasubsampling.htm
old-project: DirectShow
ms.assetid: d3308308-4bdd-46b4-a3fa-f253d552428b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: codecapi/eAVEncVideoChromaSubsampling, codecapi/eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited, codecapi/eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma, codecapi/eAVEncVideoChromaSubsamplingFormat_SameAsSource, codecapi/eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes, codecapi/eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited, dshow.eavencvideochromasubsampling, eAVEncVideoChromaSubsampling, eAVEncVideoChromaSubsampling enumeration [DirectShow], eAVEncVideoChromaSubsamplingEnumeration, eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited, eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma, eAVEncVideoChromaSubsamplingFormat_SameAsSource, eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes, eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	codecapi.h
api_name:
-	eAVEncVideoChromaSubsampling
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

