---
UID: NS:dxgi.DXGI_SURFACE_DESC
title: DXGI_SURFACE_DESC (dxgi.h)
description: Describes a surface.
helpviewer_keywords: ["93817f74-4e10-480f-7425-b90c4fe26c0d","DXGI_SURFACE_DESC","DXGI_SURFACE_DESC structure [DXGI]","direct3ddxgi.dxgi_surface_desc","dxgi/DXGI_SURFACE_DESC"]
old-location: direct3ddxgi\dxgi_surface_desc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_surface_desc.htm
ms.date: 12/05/2018
ms.keywords: 93817f74-4e10-480f-7425-b90c4fe26c0d, DXGI_SURFACE_DESC, DXGI_SURFACE_DESC structure [DXGI], direct3ddxgi.dxgi_surface_desc, dxgi/DXGI_SURFACE_DESC
req.header: dxgi.h
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
req.typenames: DXGI_SURFACE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SURFACE_DESC
 - dxgi/DXGI_SURFACE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SURFACE_DESC
---

# DXGI_SURFACE_DESC structure


## -description

Describes a surface.

## -struct-fields

### -field Width

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value describing the surface width.

### -field Height

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value describing the surface height.

### -field Format

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A member of the <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> enumerated type that describes the surface format.

### -field SampleDesc

Type: <b><a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a></b>

A member of the <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a> structure that describes multi-sampling parameters for the surface.

## -remarks

This structure is used by the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-getdesc">GetDesc</a> and  <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-createsurface">CreateSurface</a> methods.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>