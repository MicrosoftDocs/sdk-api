---
UID: NE:d2d1effects_1.D2D1_YCBCR_CHROMA_SUBSAMPLING
title: D2D1_YCBCR_CHROMA_SUBSAMPLING (d2d1effects_1.h)
description: Specifies the chroma subsampling of the input chroma image used by the YCbCr effect.
helpviewer_keywords: ["D2D1_YCBCR_CHROMA_SUBSAMPLING","D2D1_YCBCR_CHROMA_SUBSAMPLING enumeration [Direct2D]","D2D1_YCBCR_CHROMA_SUBSAMPLING_420","D2D1_YCBCR_CHROMA_SUBSAMPLING_422","D2D1_YCBCR_CHROMA_SUBSAMPLING_440","D2D1_YCBCR_CHROMA_SUBSAMPLING_444","D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO","d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING","d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_420","d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_422","d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_440","d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_444","d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO","direct2d.d2d1_ycbcr_chroma_subsampling"]
old-location: direct2d\d2d1_ycbcr_chroma_subsampling.htm
tech.root: Direct2D
ms.assetid: 4B0BDC1D-B39C-4787-90D3-50845C3A2B9A
ms.date: 12/05/2018
ms.keywords: D2D1_YCBCR_CHROMA_SUBSAMPLING, D2D1_YCBCR_CHROMA_SUBSAMPLING enumeration [Direct2D], D2D1_YCBCR_CHROMA_SUBSAMPLING_420, D2D1_YCBCR_CHROMA_SUBSAMPLING_422, D2D1_YCBCR_CHROMA_SUBSAMPLING_440, D2D1_YCBCR_CHROMA_SUBSAMPLING_444, D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO, d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING, d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_420, d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_422, d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_440, d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_444, d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO, direct2d.d2d1_ycbcr_chroma_subsampling
req.header: d2d1effects_1.h
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
req.typenames: D2D1_YCBCR_CHROMA_SUBSAMPLING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_YCBCR_CHROMA_SUBSAMPLING
 - d2d1effects_1/D2D1_YCBCR_CHROMA_SUBSAMPLING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_1.h
api_name:
 - D2D1_YCBCR_CHROMA_SUBSAMPLING
---

# D2D1_YCBCR_CHROMA_SUBSAMPLING enumeration


## -description

Specifies the chroma subsampling of the input chroma image used by the <a href="/windows/desktop/Direct2D/ycbcr-effect">YCbCr effect</a>.

## -enum-fields

### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_AUTO:0

This mode attempts to infer the chroma subsampling from the bounds of the input images. When this option is selected, 
          the smaller plane is upsampled to the size of the larger plane and this effect’s output rectangle is the intersection of the two planes. 
          When using this mode, care should be taken when applying effects to the input planes that change the image bounds, such as the border transform, 
          so that the desired size ratio between the planes is maintained.

### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_420:1

The chroma plane is horizontally subsampled by 1/2 and vertically subsampled by 1/2. 
          When this option is selected, the chroma plane is horizontally and vertically upsampled by 2x and this effect's output rectangle is the intersection of the two planes.

### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_422:2

The chroma plane is horizontally subsampled by 1/2. When this option is selected, 
          the chroma plane is horizontally upsampled by 2x and this effect's output rectangle is the intersection of the two planes.

### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_444:3

The chroma plane is not subsampled. When this option is selected this effect’s output rectangle is the intersection of the two planes.

### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_440:4

The chroma plane is vertically subsampled by 1/2. When this option is selected, the chroma plane is vertically upsampled by 2x and this effect's 
          output rectangle is the intersection of the two planes.

### -field D2D1_YCBCR_CHROMA_SUBSAMPLING_FORCE_DWORD:0xffffffff
