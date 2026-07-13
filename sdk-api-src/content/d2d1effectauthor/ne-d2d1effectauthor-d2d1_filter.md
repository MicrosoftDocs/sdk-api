---
UID: NE:d2d1effectauthor.D2D1_FILTER
title: D2D1_FILTER (d2d1effectauthor.h)
description: Represents filtering modes that a transform may select to use on input textures.
helpviewer_keywords: ["D2D1_FILTER","D2D1_FILTER enumeration [Direct2D]","D2D1_FILTER_ANISOTROPIC","D2D1_FILTER_MIN_LINEAR_MAG_MIP_POINT","D2D1_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR","D2D1_FILTER_MIN_MAG_LINEAR_MIP_POINT","D2D1_FILTER_MIN_MAG_MIP_LINEAR","D2D1_FILTER_MIN_MAG_MIP_POINT","D2D1_FILTER_MIN_MAG_POINT_MIP_LINEAR","D2D1_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT","D2D1_FILTER_MIN_POINT_MAG_MIP_LINEAR","d2d1effectauthor/D2D1_FILTER","d2d1effectauthor/D2D1_FILTER_ANISOTROPIC","d2d1effectauthor/D2D1_FILTER_MIN_LINEAR_MAG_MIP_POINT","d2d1effectauthor/D2D1_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR","d2d1effectauthor/D2D1_FILTER_MIN_MAG_LINEAR_MIP_POINT","d2d1effectauthor/D2D1_FILTER_MIN_MAG_MIP_LINEAR","d2d1effectauthor/D2D1_FILTER_MIN_MAG_MIP_POINT","d2d1effectauthor/D2D1_FILTER_MIN_MAG_POINT_MIP_LINEAR","d2d1effectauthor/D2D1_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT","d2d1effectauthor/D2D1_FILTER_MIN_POINT_MAG_MIP_LINEAR","direct2d.d2d1_filter"]
old-location: direct2d\d2d1_filter.htm
tech.root: Direct2D
ms.assetid: cd978d3c-ae41-4321-95dd-46b186acf002
ms.date: 12/05/2018
ms.keywords: D2D1_FILTER, D2D1_FILTER enumeration [Direct2D], D2D1_FILTER_ANISOTROPIC, D2D1_FILTER_MIN_LINEAR_MAG_MIP_POINT, D2D1_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR, D2D1_FILTER_MIN_MAG_LINEAR_MIP_POINT, D2D1_FILTER_MIN_MAG_MIP_LINEAR, D2D1_FILTER_MIN_MAG_MIP_POINT, D2D1_FILTER_MIN_MAG_POINT_MIP_LINEAR, D2D1_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT, D2D1_FILTER_MIN_POINT_MAG_MIP_LINEAR, d2d1effectauthor/D2D1_FILTER, d2d1effectauthor/D2D1_FILTER_ANISOTROPIC, d2d1effectauthor/D2D1_FILTER_MIN_LINEAR_MAG_MIP_POINT, d2d1effectauthor/D2D1_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR, d2d1effectauthor/D2D1_FILTER_MIN_MAG_LINEAR_MIP_POINT, d2d1effectauthor/D2D1_FILTER_MIN_MAG_MIP_LINEAR, d2d1effectauthor/D2D1_FILTER_MIN_MAG_MIP_POINT, d2d1effectauthor/D2D1_FILTER_MIN_MAG_POINT_MIP_LINEAR, d2d1effectauthor/D2D1_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT, d2d1effectauthor/D2D1_FILTER_MIN_POINT_MAG_MIP_LINEAR, direct2d.d2d1_filter
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FILTER
 - d2d1effectauthor/D2D1_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_FILTER
---

# D2D1_FILTER enumeration


## -description

Represents filtering modes that a transform may select to use on input textures.

## -enum-fields

### -field D2D1_FILTER_MIN_MAG_MIP_POINT:0x00

Use point sampling for minification, magnification, and mip-level sampling.

### -field D2D1_FILTER_MIN_MAG_POINT_MIP_LINEAR:0x01

Use point sampling for minification and magnification; use linear interpolation for mip-level sampling.

### -field D2D1_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT:0x04

Use point sampling for minification; use linear interpolation for magnification; use point sampling for mip-level sampling.

### -field D2D1_FILTER_MIN_POINT_MAG_MIP_LINEAR:0x05

Use point sampling for minification; use linear interpolation for magnification and mip-level sampling.

### -field D2D1_FILTER_MIN_LINEAR_MAG_MIP_POINT:0x10

Use linear interpolation for minification; use point sampling for magnification and mip-level sampling.

### -field D2D1_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR:0x11

Use linear interpolation for minification; use point sampling for magnification; use linear interpolation for mip-level sampling.

### -field D2D1_FILTER_MIN_MAG_LINEAR_MIP_POINT:0x14

Use linear interpolation for minification and magnification; use point sampling for mip-level sampling.

### -field D2D1_FILTER_MIN_MAG_MIP_LINEAR:0x15

Use linear interpolation for minification, magnification, and mip-level sampling.

### -field D2D1_FILTER_ANISOTROPIC:0x55

Use anisotropic interpolation for minification, magnification, and mip-level sampling.

### -field D2D1_FILTER_FORCE_DWORD:0xffffffff

## -remarks

This enumeration has the same numeric values as <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_filter">D3D11_FILTER</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_filter">D3D11_FILTER</a>
