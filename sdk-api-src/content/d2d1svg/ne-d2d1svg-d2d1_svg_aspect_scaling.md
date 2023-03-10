---
UID: NE:d2d1svg.D2D1_SVG_ASPECT_SCALING
title: D2D1_SVG_ASPECT_SCALING (d2d1svg.h)
description: The meetOrSlice portion of the SVG preserveAspectRatio attribute.
helpviewer_keywords: ["D2D1_SVG_ASPECT_SCALING","D2D1_SVG_ASPECT_SCALING enumeration [Direct2D]","D2D1_SVG_ASPECT_SCALING_FORCE_DWORD","D2D1_SVG_ASPECT_SCALING_MEET","D2D1_SVG_ASPECT_SCALING_SLICE","d2d1svg/D2D1_SVG_ASPECT_SCALING","d2d1svg/D2D1_SVG_ASPECT_SCALING_FORCE_DWORD","d2d1svg/D2D1_SVG_ASPECT_SCALING_MEET","d2d1svg/D2D1_SVG_ASPECT_SCALING_SLICE","direct2d.d2d1_svg_aspect_scaling"]
old-location: direct2d\d2d1_svg_aspect_scaling.htm
tech.root: Direct2D
ms.assetid: 9053FD0F-7A6C-473D-AB88-C5555A8E1652
ms.date: 12/05/2018
ms.keywords: D2D1_SVG_ASPECT_SCALING, D2D1_SVG_ASPECT_SCALING enumeration [Direct2D], D2D1_SVG_ASPECT_SCALING_FORCE_DWORD, D2D1_SVG_ASPECT_SCALING_MEET, D2D1_SVG_ASPECT_SCALING_SLICE, d2d1svg/D2D1_SVG_ASPECT_SCALING, d2d1svg/D2D1_SVG_ASPECT_SCALING_FORCE_DWORD, d2d1svg/D2D1_SVG_ASPECT_SCALING_MEET, d2d1svg/D2D1_SVG_ASPECT_SCALING_SLICE, direct2d.d2d1_svg_aspect_scaling
req.header: d2d1svg.h
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
req.typenames: D2D1_SVG_ASPECT_SCALING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SVG_ASPECT_SCALING
 - d2d1svg/D2D1_SVG_ASPECT_SCALING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1svg.h
api_name:
 - D2D1_SVG_ASPECT_SCALING
---

# D2D1_SVG_ASPECT_SCALING enumeration


## -description

The meetOrSlice portion of the SVG preserveAspectRatio attribute.

## -enum-fields

### -field D2D1_SVG_ASPECT_SCALING_MEET:0

Scale the viewBox up as much as possible such that the entire viewBox is visible within the viewport.

### -field D2D1_SVG_ASPECT_SCALING_SLICE:1

Scale the viewBox down as much as possible such that the entire viewport is
          covered by the viewBox.

### -field D2D1_SVG_ASPECT_SCALING_FORCE_DWORD:0xffffffff

