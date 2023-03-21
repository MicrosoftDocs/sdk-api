---
UID: NE:codecapi.eAVEncVideoChromaSubsampling
title: eAVEncVideoChromaSubsampling (codecapi.h)
description: Specifies chroma siting. Chroma siting defines the positions of the chroma samples relative to the luma samples. This enumeration is used with the AVEncVideoInputChromaSubsampling and AVEncVideoOutputChromaSubsampling properties.
helpviewer_keywords: ["codecapi/eAVEncVideoChromaSubsampling","codecapi/eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited","codecapi/eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma","codecapi/eAVEncVideoChromaSubsamplingFormat_SameAsSource","codecapi/eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes","codecapi/eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited","dshow.eavencvideochromasubsampling","eAVEncVideoChromaSubsampling","eAVEncVideoChromaSubsampling enumeration [DirectShow]","eAVEncVideoChromaSubsamplingEnumeration","eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited","eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma","eAVEncVideoChromaSubsamplingFormat_SameAsSource","eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes","eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited"]
old-location: dshow\eavencvideochromasubsampling.htm
tech.root: dshow
ms.assetid: d3308308-4bdd-46b4-a3fa-f253d552428b
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoChromaSubsampling, codecapi/eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited, codecapi/eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma, codecapi/eAVEncVideoChromaSubsamplingFormat_SameAsSource, codecapi/eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes, codecapi/eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited, dshow.eavencvideochromasubsampling, eAVEncVideoChromaSubsampling, eAVEncVideoChromaSubsampling enumeration [DirectShow], eAVEncVideoChromaSubsamplingEnumeration, eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited, eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma, eAVEncVideoChromaSubsamplingFormat_SameAsSource, eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes, eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVEncVideoChromaSubsampling
 - codecapi/eAVEncVideoChromaSubsampling
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoChromaSubsampling
---

# eAVEncVideoChromaSubsampling enumeration


## -description

Specifies chroma siting. Chroma siting defines the positions of the chroma samples relative to the luma samples. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoinputchromasubsampling-property">AVEncVideoInputChromaSubsampling</a> and <a href="/windows/desktop/DirectShow/avencvideooutputchromasubsampling-property">AVEncVideoOutputChromaSubsampling</a> properties.

## -enum-fields

### -field eAVEncVideoChromaSubsamplingFormat_SameAsSource:0

Use the same chroma siting as the input video. This flag applies to the <b>AVEncVideoOutputChromaResolution</b> property only. This flag may not be combined with other flags.

### -field eAVEncVideoChromaSubsamplingFormat_ProgressiveChroma:0x8

Chroma should be reconstructed as if the underlying video was progressive content, rather than skipping fields or applying chroma filtering to minimize artifacts from reconstructing 4:2:0 interlaced chroma.

### -field eAVEncVideoChromaSubsamplingFormat_Horizontally_Cosited:0x4

Chroma samples are aligned horizontally with multiples of the luma samples.

### -field eAVEncVideoChromaSubsamplingFormat_Vertically_Cosited:0x2

Chroma samples are aligned vertically with multiples of the luma samples.

### -field eAVEncVideoChromaSubsamplingFormat_Vertically_AlignedChromaPlanes:0x1

The chroma planes have the same phase alignment. It is not valid to omit this flag unless the data is vertically cosited. If the data is not vertically cosited, this flag is required. If this flag is absent, the Cb and Cr samples are sited on alternate lines. For example, interlaced PAL DV video uses non-aligned chroma planes.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
