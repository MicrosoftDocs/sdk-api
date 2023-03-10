---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0013_0002
title: VMR9DeinterlaceTech (vmr9.h)
description: The VMR9DeinterlaceTech enumeration type describes the algorithm used for deinterlacing a video stream. The flags are not mutually exclusive; drivers can set a combination of flags.
helpviewer_keywords: ["DeinterlaceTech9_BOBLineReplicate","DeinterlaceTech9_BOBVerticalStretch","DeinterlaceTech9_EdgeFiltering","DeinterlaceTech9_FieldAdaptive","DeinterlaceTech9_MedianFiltering","DeinterlaceTech9_MotionVectorSteered","DeinterlaceTech9_PixelAdaptive","DeinterlaceTech9_Unknown","VMR9DeinterlaceTech","VMR9DeinterlaceTech","VMR9DeinterlaceTech enumeration [DirectShow]","VMR9DeinterlaceTechEnumeration","dshow.vmr9deinterlacetech","vmr9/DeinterlaceTech9_BOBLineReplicate","vmr9/DeinterlaceTech9_BOBVerticalStretch","vmr9/DeinterlaceTech9_EdgeFiltering","vmr9/DeinterlaceTech9_FieldAdaptive","vmr9/DeinterlaceTech9_MedianFiltering","vmr9/DeinterlaceTech9_MotionVectorSteered","vmr9/DeinterlaceTech9_PixelAdaptive","vmr9/DeinterlaceTech9_Unknown","vmr9/VMR9DeinterlaceTech"]
old-location: dshow\vmr9deinterlacetech.htm
tech.root: dshow
ms.assetid: 2b0b56b7-bab3-4184-a453-2da880aa38c9
ms.date: 12/05/2018
ms.keywords: DeinterlaceTech9_BOBLineReplicate, DeinterlaceTech9_BOBVerticalStretch, DeinterlaceTech9_EdgeFiltering, DeinterlaceTech9_FieldAdaptive, DeinterlaceTech9_MedianFiltering, DeinterlaceTech9_MotionVectorSteered, DeinterlaceTech9_PixelAdaptive, DeinterlaceTech9_Unknown, VMR9DeinterlaceTech, VMR9DeinterlaceTech , VMR9DeinterlaceTech enumeration [DirectShow], VMR9DeinterlaceTechEnumeration, dshow.vmr9deinterlacetech, vmr9/DeinterlaceTech9_BOBLineReplicate, vmr9/DeinterlaceTech9_BOBVerticalStretch, vmr9/DeinterlaceTech9_EdgeFiltering, vmr9/DeinterlaceTech9_FieldAdaptive, vmr9/DeinterlaceTech9_MedianFiltering, vmr9/DeinterlaceTech9_MotionVectorSteered, vmr9/DeinterlaceTech9_PixelAdaptive, vmr9/DeinterlaceTech9_Unknown, vmr9/VMR9DeinterlaceTech
req.header: vmr9.h
req.include-header: 
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
req.typenames: VMR9DeinterlaceTech
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0013_0002
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0013_0002
 - VMR9DeinterlaceTech
 - vmr9/VMR9DeinterlaceTech
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9DeinterlaceTech
---

# VMR9DeinterlaceTech enumeration


## -description

The <code>VMR9DeinterlaceTech</code> enumeration type describes the algorithm used for deinterlacing a video stream. The flags are not mutually exclusive; drivers can set a combination of flags.

## -enum-fields

### -field DeinterlaceTech9_Unknown:0

The algorithm is unknown or proprietary.

### -field DeinterlaceTech9_BOBLineReplicate:0x1

The algorithm creates each missing line by repeating the line above it or below it. This method creates jagged artifacts and is not recommended.

### -field DeinterlaceTech9_BOBVerticalStretch:0x2

The algorithm creates the missing lines by vertically stretching each video field by a factor of two. For example, it might average two lines or use a (-1, 9, 9, -1)/16 filter across four lines. Slight vertical adjustments are made to ensure that the resulting image does not "bob" up and down

### -field DeinterlaceTech9_MedianFiltering:0x4

The algorithm uses median filtering to recreate the pixels in the missing lines.

### -field DeinterlaceTech9_EdgeFiltering:0x10

The algorithm uses an edge filter to create the missing lines. In this process, spatial directional filters are applied to determine the orientation of edges in the picture content. Missing pixels are created by filtering along (rather than across) the detected edges.

### -field DeinterlaceTech9_FieldAdaptive:0x20

The algorithm uses spatial or temporal interpolation, switching between the two on a field-by-field basis, depending on the amount of motion.

### -field DeinterlaceTech9_PixelAdaptive:0x40

The algorithm uses spatial or temporal interpolation, switching between the two on a pixel-by-pixel basis, depending on the amount of motion.

### -field DeinterlaceTech9_MotionVectorSteered:0x80

The algorithm identifies objects within a sequence of video fields. Before it recreates the missing pixels, it aligns the movement axes of the individual objects in the scene to make them parallel with the time axis.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9deinterlacecaps">VMR9DeinterlaceCaps Structure</a>
