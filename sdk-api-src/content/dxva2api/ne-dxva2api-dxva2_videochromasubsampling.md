---
UID: NE:dxva2api._DXVA2_VideoChromaSubSampling
title: DXVA2_VideoChromaSubSampling (dxva2api.h)
description: Describes how chroma values are positioned relative to the luma samples in a YUV video frame.
helpviewer_keywords: ["0f9d63fd-46fa-498c-8703-1beeaf09ce86","DXVA2_VideoChromaSubSampling","DXVA2_VideoChromaSubSampling enumeration [Media Foundation]","DXVA2_VideoChromaSubsamplingMask","DXVA2_VideoChromaSubsampling_Cosited","DXVA2_VideoChromaSubsampling_DV_PAL","DXVA2_VideoChromaSubsampling_Horizontally_Cosited","DXVA2_VideoChromaSubsampling_MPEG1","DXVA2_VideoChromaSubsampling_MPEG2","DXVA2_VideoChromaSubsampling_ProgressiveChroma","DXVA2_VideoChromaSubsampling_Unknown","DXVA2_VideoChromaSubsampling_Vertically_AlignedChromaPlanes","DXVA2_VideoChromaSubsampling_Vertically_Cosited","dxva2api/DXVA2_VideoChromaSubSampling","dxva2api/DXVA2_VideoChromaSubsamplingMask","dxva2api/DXVA2_VideoChromaSubsampling_Cosited","dxva2api/DXVA2_VideoChromaSubsampling_DV_PAL","dxva2api/DXVA2_VideoChromaSubsampling_Horizontally_Cosited","dxva2api/DXVA2_VideoChromaSubsampling_MPEG1","dxva2api/DXVA2_VideoChromaSubsampling_MPEG2","dxva2api/DXVA2_VideoChromaSubsampling_ProgressiveChroma","dxva2api/DXVA2_VideoChromaSubsampling_Unknown","dxva2api/DXVA2_VideoChromaSubsampling_Vertically_AlignedChromaPlanes","dxva2api/DXVA2_VideoChromaSubsampling_Vertically_Cosited","mf.dxva2_videochromasubsampling"]
old-location: mf\dxva2_videochromasubsampling.htm
tech.root: mf
ms.assetid: 0f9d63fd-46fa-498c-8703-1beeaf09ce86
ms.date: 12/05/2018
ms.keywords: 0f9d63fd-46fa-498c-8703-1beeaf09ce86, DXVA2_VideoChromaSubSampling, DXVA2_VideoChromaSubSampling enumeration [Media Foundation], DXVA2_VideoChromaSubsamplingMask, DXVA2_VideoChromaSubsampling_Cosited, DXVA2_VideoChromaSubsampling_DV_PAL, DXVA2_VideoChromaSubsampling_Horizontally_Cosited, DXVA2_VideoChromaSubsampling_MPEG1, DXVA2_VideoChromaSubsampling_MPEG2, DXVA2_VideoChromaSubsampling_ProgressiveChroma, DXVA2_VideoChromaSubsampling_Unknown, DXVA2_VideoChromaSubsampling_Vertically_AlignedChromaPlanes, DXVA2_VideoChromaSubsampling_Vertically_Cosited, dxva2api/DXVA2_VideoChromaSubSampling, dxva2api/DXVA2_VideoChromaSubsamplingMask, dxva2api/DXVA2_VideoChromaSubsampling_Cosited, dxva2api/DXVA2_VideoChromaSubsampling_DV_PAL, dxva2api/DXVA2_VideoChromaSubsampling_Horizontally_Cosited, dxva2api/DXVA2_VideoChromaSubsampling_MPEG1, dxva2api/DXVA2_VideoChromaSubsampling_MPEG2, dxva2api/DXVA2_VideoChromaSubsampling_ProgressiveChroma, dxva2api/DXVA2_VideoChromaSubsampling_Unknown, dxva2api/DXVA2_VideoChromaSubsampling_Vertically_AlignedChromaPlanes, dxva2api/DXVA2_VideoChromaSubsampling_Vertically_Cosited, mf.dxva2_videochromasubsampling
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVA2_VideoChromaSubSampling
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_VideoChromaSubSampling
 - dxva2api/_DXVA2_VideoChromaSubSampling
 - DXVA2_VideoChromaSubSampling
 - dxva2api/DXVA2_VideoChromaSubSampling
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_VideoChromaSubSampling
---

# DXVA2_VideoChromaSubSampling enumeration


## -description

Describes how chroma values are positioned relative to the luma samples in a YUV video frame. These flags are used in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat">DXVA2_ExtendedFormat</a> structure.

## -enum-fields

### -field DXVA2_VideoChromaSubsamplingMask:0xf

Bitmask to validate flag values. This value is not a valid flag.

### -field DXVA2_VideoChromaSubsampling_Unknown:0

Unknown encoding scheme.

### -field DXVA2_VideoChromaSubsampling_ProgressiveChroma:0x8

Chroma should be reconstructed as if the underlying video was progressive content, rather than skipping fields or applying chroma filtering to minimize artifacts from reconstructing 4:2:0 interlaced chroma.

### -field DXVA2_VideoChromaSubsampling_Horizontally_Cosited:0x4

Horizontally cosited. Chroma samples are aligned horizontally with multiples of the luma samples. If this flag is not set, chroma samples are located 1/2 pixel to the right of the corresponding luma samples.

### -field DXVA2_VideoChromaSubsampling_Vertically_Cosited:0x2

Vertically cosited. Chroma samples are aligned vertically with multiples of the luma samples. If this flag is not set, chroma samples are located 1/2 pixel down from the corresponding luma samples.

### -field DXVA2_VideoChromaSubsampling_Vertically_AlignedChromaPlanes:0x1

The chroma planes are vertically aligned. If this flag is not set, chroma planes are out of phase by 1/2 chroma sample, and the Cb and Cr samples are sited on alternate lines.

### -field DXVA2_VideoChromaSubsampling_MPEG2

Specifies the chroma encoding scheme for MPEG-2 video. Chroma samples are aligned horizontally with the luma samples, but are not aligned vertically. The U and V planes are aligned vertically.

### -field DXVA2_VideoChromaSubsampling_MPEG1

Specifies the chroma encoding scheme for MPEG-1 video.

### -field DXVA2_VideoChromaSubsampling_DV_PAL

Specifies the chroma encoding scheme for PAL DV video.

### -field DXVA2_VideoChromaSubsampling_Cosited

Horizontally and vertically cosited. Chroma samples are aligned vertically and horizontally with the luma samples. YUV formats such as 4:4:4, 4:2:2, and 4:1:1 are always cosited in both directions and should use this flag.

## -remarks

The following diagrams show the most common arrangements.

<h3><a id="4_4_4_horizontally_and_vertically_cosited._________"></a><a id="4_4_4_HORIZONTALLY_AND_VERTICALLY_COSITED._________"></a>4:4:4 horizontally and vertically cosited.
        </h3>
<img alt="Diagram showing 4x4 grid; each cell contains two circles--one for luma and one for chroma " border="" src="images/1a4cc0bf-87e4-4695-a14f-2f8a653f7ba9.gif"/>
<h3><a id="4_2_2_horizontally_and_vertically_cosited._________"></a><a id="4_2_2_HORIZONTALLY_AND_VERTICALLY_COSITED._________"></a>4:2:2 horizontally and vertically cosited.
        </h3>
<img alt="Diagram similar to the original one, but cells in the second and fourth columns have luma but not chroma" border="" src="images/11280687-7d75-4b6d-9e69-d78d767f3491.gif"/>
<h3><a id="4_1_1_horizontally_and_vertically_cosited._________"></a><a id="4_1_1_HORIZONTALLY_AND_VERTICALLY_COSITED._________"></a>4:1:1 horizontally and vertically cosited.
        </h3>
<img alt="Diagram similar to the original one, but only cells in the first column contain chroma " border="" src="images/7443405f-735c-44fd-ad09-613f696eadf3.gif"/>
<h3><a id="4_2_0_progressive__horizontally_cosited._________"></a><a id="4_2_0_PROGRESSIVE__HORIZONTALLY_COSITED._________"></a>4:2:0 progressive, horizontally cosited.
        </h3>
<img alt="Diagram similar to the original one, but chroma circles appear only on odd-numbered row boundaries in odd-numbered columns" border="" src="images/ba14c38b-bcab-4e68-ab24-e4a9162ce12f.gif"/>
Example: MPEG-2 progressive.

<h3><a id="4_2_0_progressive__not_cosited_horizontally_or_vertically._________"></a><a id="4_2_0_PROGRESSIVE__NOT_COSITED_HORIZONTALLY_OR_VERTICALLY._________"></a>4:2:0 progressive, not cosited horizontally or vertically.
        </h3>
<img alt="Diagram similar to the original one, but chroma circles appear only at intersections of odd-numbered row boundaries and odd-numbered columns boundaries" border="" src="images/6fec0c32-14a9-43d2-9703-f3e5df2dc7a0.gif"/>
Example: JPEG progressive.

<h3><a id="4_2_0_interlaced__vertically_cosited__chroma_planes_out_of_phase._________"></a><a id="4_2_0_INTERLACED__VERTICALLY_COSITED__CHROMA_PLANES_OUT_OF_PHASE._________"></a>4:2:0 interlaced, vertically cosited; chroma planes out of phase.
        </h3>
<img alt="Diagram showing two 4x4 matrices; one is lower than the other by half the width of a row, and chroma circles in each column alternate between Cr and Cb" border="" src="images/f75760b6-59d2-4865-803d-e7ea5dd65914.gif"/>
Example: DV PAL interlaced.

<h3><a id="4_2_0_interlaced__horizontally_cosited._________"></a><a id="4_2_0_INTERLACED__HORIZONTALLY_COSITED._________"></a>4:2:0 interlaced, horizontally cosited.
        </h3>
<img alt="Diagram showing two instances of the fourth diagram; one is lower than the other by half the width of a row" border="" src="images/c09b7773-fcb7-4949-a894-1d35a113ed9b.gif"/>
Example: MPEG-2 interlaced.

This enumeration is equivalent to the DXVA_VideoChromaSubsampling enumeration used in DXVA 1.0.
      

If you are using the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface to describe the video format, chroma siting is specified in the <a href="/windows/desktop/medfound/mf-mt-video-chroma-siting-attribute">MF_MT_VIDEO_CHROMA_SITING</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
