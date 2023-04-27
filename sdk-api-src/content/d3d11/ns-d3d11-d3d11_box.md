---
UID: NS:d3d11.D3D11_BOX
title: D3D11_BOX (d3d11.h)
description: Defines a 3D box. (D3D11_BOX)
helpviewer_keywords: ["D3D11_BOX","D3D11_BOX structure [Direct3D 11]","b76b0218-be11-7108-701a-e9002dd6f441","d3d11/D3D11_BOX","direct3d11.d3d11_box"]
old-location: direct3d11\d3d11_box.htm
tech.root: direct3d11
ms.assetid: 0cc98805-a36e-41aa-a24f-51fbcf5070df
ms.date: 12/05/2018
ms.keywords: D3D11_BOX, D3D11_BOX structure [Direct3D 11], b76b0218-be11-7108-701a-e9002dd6f441, d3d11/D3D11_BOX, direct3d11.d3d11_box
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
req.typenames: D3D11_BOX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BOX
 - d3d11/D3D11_BOX
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
 - D3D11_BOX
---

# D3D11_BOX structure


## -description

Defines a 3D box.

## -struct-fields

### -field left

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The x position of the left hand side of the box.

### -field top

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The y position of the top of the box.

### -field front

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The z position of the front of the box.

### -field right

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The x position of the right hand side of the box.

### -field bottom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The y position of the bottom of the box.

### -field back

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The z position of the back of the box.

## -remarks

The following diagram shows a 3D box, where the origin is the left, front, top corner.

<img alt="Diagram of a 3D box, where the origin is the left, front, top corner" src="./images/D3D10_box.png"/>

The values for <b>right</b>, <b>bottom</b>, and <b>back</b> are each one pixel past the end of the pixels that are included in the box region.  That is, the values for <b>left</b>, <b>top</b>, and <b>front</b> are included in the box region while the values for right, bottom, and back are excluded from the box region. For example, for a box that is one pixel wide, (right - left) == 1; the box region includes the left pixel but not the right pixel.

Coordinates of a box are in bytes for buffers and in texels for textures.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
