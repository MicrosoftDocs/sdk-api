---
UID: NE:strmif.VMRDeinterlaceTech
title: VMRDeinterlaceTech (strmif.h)
description: The VMRDeinterlaceTech enumeration type describes the algorithm used for deinterlacing a video stream. The flags are not mutually exclusive; drivers can set a combination of flags.
helpviewer_keywords: ["DeinterlaceTech_BOBLineReplicate","DeinterlaceTech_BOBVerticalStretch","DeinterlaceTech_EdgeFiltering","DeinterlaceTech_FieldAdaptive","DeinterlaceTech_MedianFiltering","DeinterlaceTech_MotionVectorSteered","DeinterlaceTech_PixelAdaptive","DeinterlaceTech_Unknown","VMRDeinterlaceTech","VMRDeinterlaceTech enumeration [DirectShow]","VMRDeinterlaceTechEnumeration","dshow.vmrdeinterlacetech","strmif/DeinterlaceTech_BOBLineReplicate","strmif/DeinterlaceTech_BOBVerticalStretch","strmif/DeinterlaceTech_EdgeFiltering","strmif/DeinterlaceTech_FieldAdaptive","strmif/DeinterlaceTech_MedianFiltering","strmif/DeinterlaceTech_MotionVectorSteered","strmif/DeinterlaceTech_PixelAdaptive","strmif/DeinterlaceTech_Unknown","strmif/VMRDeinterlaceTech"]
old-location: dshow\vmrdeinterlacetech.htm
tech.root: dshow
ms.assetid: 10149023-c5e8-4dce-8a8c-cde96ae6c073
ms.date: 12/05/2018
ms.keywords: DeinterlaceTech_BOBLineReplicate, DeinterlaceTech_BOBVerticalStretch, DeinterlaceTech_EdgeFiltering, DeinterlaceTech_FieldAdaptive, DeinterlaceTech_MedianFiltering, DeinterlaceTech_MotionVectorSteered, DeinterlaceTech_PixelAdaptive, DeinterlaceTech_Unknown, VMRDeinterlaceTech, VMRDeinterlaceTech enumeration [DirectShow], VMRDeinterlaceTechEnumeration, dshow.vmrdeinterlacetech, strmif/DeinterlaceTech_BOBLineReplicate, strmif/DeinterlaceTech_BOBVerticalStretch, strmif/DeinterlaceTech_EdgeFiltering, strmif/DeinterlaceTech_FieldAdaptive, strmif/DeinterlaceTech_MedianFiltering, strmif/DeinterlaceTech_MotionVectorSteered, strmif/DeinterlaceTech_PixelAdaptive, strmif/DeinterlaceTech_Unknown, strmif/VMRDeinterlaceTech
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VMRDeinterlaceTech
req.redist: 
req.product: Windows XP with SP1
ms.custom: 19H1
f1_keywords:
 - VMRDeinterlaceTech
 - strmif/VMRDeinterlaceTech
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRDeinterlaceTech
---

# VMRDeinterlaceTech enumeration


## -description

The <b>VMRDeinterlaceTech</b> enumeration type describes the algorithm used for deinterlacing a video stream. The flags are not mutually exclusive; drivers can set a combination of flags.

## -enum-fields

### -field DeinterlaceTech_Unknown:0

The algorithm is unknown or proprietary.

### -field DeinterlaceTech_BOBLineReplicate:0x1

The algorithm creates each missing line by repeating the line above it or below it. This method creates jagged artifacts and is not recommended.

### -field DeinterlaceTech_BOBVerticalStretch:0x2

The algorithm creates the missing lines by vertically stretching each video field by a factor of two. For example, it might average two lines or use a (-1, 9, 9, -1)/16 filter across four lines. Slight vertical adjustments are made to ensure that the resulting image does not "bob" up and down.

### -field DeinterlaceTech_MedianFiltering:0x4

The algorithm uses median filtering to recreate the pixels in the missing lines.

### -field DeinterlaceTech_EdgeFiltering:0x10

The algorithm uses an edge filter to create the missing lines. In this process, spatial directional filters are applied to determine the orientation of edges in the picture content. Missing pixels are created by filtering along (rather than across) the detected edges.

### -field DeinterlaceTech_FieldAdaptive:0x20

The algorithm uses spatial or temporal interpolation, switching between the two on a field-by-field basis, depending on the amount of motion.

### -field DeinterlaceTech_PixelAdaptive:0x40

The algorithm uses spatial or temporal interpolation, switching between the two on a pixel-by-pixel basis, depending on the amount of motion.

### -field DeinterlaceTech_MotionVectorSteered:0x80

The algorithm identifies objects within a sequence of video fields. Before it recreates the missing pixels, it aligns the movement axes of the individual objects in the scene to make them parallel with the time axis.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



[VMRDeinterlaceCaps Structure](/windows/desktop/api/strmif/ns-strmif-vmrdeinterlacecaps)
