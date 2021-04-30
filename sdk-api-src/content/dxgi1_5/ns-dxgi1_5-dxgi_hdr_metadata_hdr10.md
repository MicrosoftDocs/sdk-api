---
UID: NS:dxgi1_5.DXGI_HDR_METADATA_HDR10
title: DXGI_HDR_METADATA_HDR10 (dxgi1_5.h)
description: Describes the metadata for HDR10, used when video is compressed using High Efficiency Video Coding (HEVC).
helpviewer_keywords: ["DXGI_HDR_METADATA_HDR10","DXGI_HDR_METADATA_HDR10 structure [DXGI]","direct3ddxgi.dxgi_hdr_metadata_hdr10","dxgi1_5/DXGI_HDR_METADATA_HDR10"]
old-location: direct3ddxgi\dxgi_hdr_metadata_hdr10.htm
tech.root: direct3ddxgi
ms.assetid: 67A53A43-121F-4D83-AACC-D25D58123BE1
ms.date: 12/05/2018
ms.keywords: DXGI_HDR_METADATA_HDR10, DXGI_HDR_METADATA_HDR10 structure [DXGI], direct3ddxgi.dxgi_hdr_metadata_hdr10, dxgi1_5/DXGI_HDR_METADATA_HDR10
req.header: dxgi1_5.h
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
req.typenames: DXGI_HDR_METADATA_HDR10
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_HDR_METADATA_HDR10
 - dxgi1_5/DXGI_HDR_METADATA_HDR10
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_5.h
api_name:
 - DXGI_HDR_METADATA_HDR10
---

# DXGI_HDR_METADATA_HDR10 structure


## -description

Describes the metadata for HDR10, used when video is compressed using High Efficiency Video Coding (HEVC). This is used to describe the capabilities of the display used to master the content and the luminance values of the content.

## -struct-fields

### -field RedPrimary

The chromaticity coordinates of the red value in the CIE1931 color space. Index 0 contains the X coordinate and index 1 contains the Y coordinate. The values are normalized to 50,000.

### -field GreenPrimary

The chromaticity coordinates of the green value in the CIE1931 color space. Index 0 contains the X coordinate and index 1 contains the Y coordinate. The values are normalized to 50,000.

### -field BluePrimary

The chromaticity coordinates of the blue value in the CIE1931 color space. Index 0 contains the X coordinate and index 1 contains the Y coordinate. The values are normalized to 50,000.

### -field WhitePoint

The chromaticity coordinates of the white point in the CIE1931 color space. Index 0 contains the X coordinate and index 1 contains the Y coordinate. The values are normalized to 50,000.

### -field MaxMasteringLuminance

The maximum number of nits of the display used to master the content. Values are in whole nits.

### -field MinMasteringLuminance

The minimum number of nits of the display used to master the content. Values are 1/10000th of a nit (0.0001 nit).

### -field MaxContentLightLevel

The maximum content light level (MaxCLL). This is the nit value corresponding to the brightest pixel used anywhere in the content.

### -field MaxFrameAverageLightLevel

The maximum frame average light level (MaxFALL). This is the nit value corresponding to the average luminance of the frame which has the brightest average luminance anywhere in the content.

## -remarks

This structure represents the definition of HDR10 metadata used with HEVC, not HDR10 metadata for ST.2086. These are closely related but defined differently.

Example: Mastering display with DCI-P3 color primaries and D65 white point, maximum luminance of 1000 nits and minimum luminance of 0.001 nits; content has maximum luminance of 2000 nits and maximum frame average light level (MaxFALL) of 500 nits.


```cpp
RedPrimary[0] = 0.680 * 50000;
RedPrimary[1] = 0.320 * 50000;
GreenPrimary[0] = 0.265 * 50000;
GreenPrimary[1] = 0.690 * 50000;
BluePrimary[0] = 0.150 * 50000;
BluePrimary[1] = 0.060 * 50000;
WhitePoint[0] = 0.3127 * 50000;
WhitePoint[1] = 0.3290 * 50000;
MaxMasteringLuminance = 1000;
MinMasteringLuminance = 0.001 * 10000;
MaxContentLightLevel = 2000;
MaxFrameAverageLightLevel = 500;
```


This structure is used in conjunction with the <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgiswapchain4-sethdrmetadata">SetHDRMetaData</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/dxgi-1-5-improvements">DXGI 1.5 Improvements</a>



<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
