---
UID: NE:d3d11.D3D11_COLOR_WRITE_ENABLE
title: D3D11_COLOR_WRITE_ENABLE (d3d11.h)
description: Identify which components of each pixel of a render target are writable during blending.
helpviewer_keywords: ["D3D11_COLOR_WRITE_ENABLE","D3D11_COLOR_WRITE_ENABLE enumeration [Direct3D 11]","D3D11_COLOR_WRITE_ENABLE_ALL","D3D11_COLOR_WRITE_ENABLE_ALPHA","D3D11_COLOR_WRITE_ENABLE_BLUE","D3D11_COLOR_WRITE_ENABLE_GREEN","D3D11_COLOR_WRITE_ENABLE_RED","d3d11/D3D11_COLOR_WRITE_ENABLE","d3d11/D3D11_COLOR_WRITE_ENABLE_ALL","d3d11/D3D11_COLOR_WRITE_ENABLE_ALPHA","d3d11/D3D11_COLOR_WRITE_ENABLE_BLUE","d3d11/D3D11_COLOR_WRITE_ENABLE_GREEN","d3d11/D3D11_COLOR_WRITE_ENABLE_RED","direct3d11.d3d11_color_write_enable","f4a83aa2-659b-6119-cd72-8cca8897c5a5"]
old-location: direct3d11\d3d11_color_write_enable.htm
tech.root: direct3d11
ms.assetid: 3ff16c92-ef9c-4a59-8868-3b2cfe1b0e38
ms.date: 12/05/2018
ms.keywords: D3D11_COLOR_WRITE_ENABLE, D3D11_COLOR_WRITE_ENABLE enumeration [Direct3D 11], D3D11_COLOR_WRITE_ENABLE_ALL, D3D11_COLOR_WRITE_ENABLE_ALPHA, D3D11_COLOR_WRITE_ENABLE_BLUE, D3D11_COLOR_WRITE_ENABLE_GREEN, D3D11_COLOR_WRITE_ENABLE_RED, d3d11/D3D11_COLOR_WRITE_ENABLE, d3d11/D3D11_COLOR_WRITE_ENABLE_ALL, d3d11/D3D11_COLOR_WRITE_ENABLE_ALPHA, d3d11/D3D11_COLOR_WRITE_ENABLE_BLUE, d3d11/D3D11_COLOR_WRITE_ENABLE_GREEN, d3d11/D3D11_COLOR_WRITE_ENABLE_RED, direct3d11.d3d11_color_write_enable, f4a83aa2-659b-6119-cd72-8cca8897c5a5
req.header: d3d11.h
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
req.typenames: D3D11_COLOR_WRITE_ENABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_COLOR_WRITE_ENABLE
 - d3d11/D3D11_COLOR_WRITE_ENABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_COLOR_WRITE_ENABLE
---

# D3D11_COLOR_WRITE_ENABLE enumeration


## -description

Identify which components of each pixel of a render target are writable during blending.

## -enum-fields

### -field D3D11_COLOR_WRITE_ENABLE_RED:1

Allow data to be stored in the red component.

### -field D3D11_COLOR_WRITE_ENABLE_GREEN:2

Allow data to be stored in the green component.

### -field D3D11_COLOR_WRITE_ENABLE_BLUE:4

Allow data to be stored in the blue component.

### -field D3D11_COLOR_WRITE_ENABLE_ALPHA:8

Allow data to be stored in the alpha component.

### -field D3D11_COLOR_WRITE_ENABLE_ALL

Allow data to be stored in all components.

## -remarks

These flags can be combined with a bitwise OR.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
