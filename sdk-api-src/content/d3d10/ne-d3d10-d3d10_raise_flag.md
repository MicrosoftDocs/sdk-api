---
UID: NE:d3d10.D3D10_RAISE_FLAG
title: D3D10_RAISE_FLAG (d3d10.h)
description: Option(s) for raising an error to a non-continuable exception.
helpviewer_keywords: ["4f0a160b-254f-303d-968b-d35d73102d48","D3D10_RAISE_FLAG","D3D10_RAISE_FLAG enumeration [Direct3D 10]","D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR","d3d10/D3D10_RAISE_FLAG","d3d10/D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR","direct3d10.d3d10_raise_flag"]
old-location: direct3d10\d3d10_raise_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_raise_flag.htm
ms.date: 12/05/2018
ms.keywords: 4f0a160b-254f-303d-968b-d35d73102d48, D3D10_RAISE_FLAG, D3D10_RAISE_FLAG enumeration [Direct3D 10], D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR, d3d10/D3D10_RAISE_FLAG, d3d10/D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR, direct3d10.d3d10_raise_flag
req.header: d3d10.h
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
req.typenames: D3D10_RAISE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_RAISE_FLAG
 - d3d10/D3D10_RAISE_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RAISE_FLAG
---

# D3D10_RAISE_FLAG enumeration


## -description

Option(s) for raising an error to a non-continuable exception.

## -enum-fields

### -field D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR:0x1L

Raise an internal driver error to a non-continuable exception.

## -remarks

These flags are used by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getexceptionmode">ID3D10Device::GetExceptionMode</a> and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-setexceptionmode">ID3D10Device::SetExceptionMode</a>. Use 0 to indicate no flags; multiple flags can be logically OR'ed together.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
