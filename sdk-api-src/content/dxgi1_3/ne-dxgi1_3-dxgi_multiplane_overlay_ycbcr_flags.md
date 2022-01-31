---
UID: NE:dxgi1_3.DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
title: DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS (dxgi1_3.h)
description: Options for swap-chain color space.
helpviewer_keywords: ["DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS","DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS enumeration [DXGI]","DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709","DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE","DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC","direct3ddxgi.dxgi_multiplane_overlay_ycbcr_flags","dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS","dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709","dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE","dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC"]
old-location: direct3ddxgi\dxgi_multiplane_overlay_ycbcr_flags.htm
tech.root: direct3ddxgi
ms.assetid: 8BD502DC-39C1-472E-AC29-14A1F7EDB37E
ms.date: 12/05/2018
ms.keywords: DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS, DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS enumeration [DXGI], DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709, DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE, DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC, direct3ddxgi.dxgi_multiplane_overlay_ycbcr_flags, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC
req.header: dxgi1_3.h
req.include-header: DXGIPartner.h
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
req.typenames: DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
 - dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
---

# DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS enumeration


## -description

Options for swap-chain color space.

## -enum-fields

### -field DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE:0x1

Specifies nominal range YCbCr, which isn't an absolute color space, but a way of encoding RGB info.

### -field DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709:0x2

Specifies BT.709, which standardizes the format of high-definition television and has 16:9 (widescreen) aspect ratio.

### -field DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC:0x4

Specifies xvYCC or extended-gamut YCC (also x.v.Color) color space that can be used in the video electronics of television sets to support a gamut 1.8 times as large as that of the sRGB color space.

## -remarks

This enum is used by <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-setcolorspace">SetColorSpace</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
