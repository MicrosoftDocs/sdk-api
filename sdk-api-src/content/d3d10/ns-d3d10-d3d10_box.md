---
UID: NS:d3d10.D3D10_BOX
title: D3D10_BOX (d3d10.h)
description: Defines a 3D box. (D3D10_BOX)
helpviewer_keywords: ["D3D10_BOX","D3D10_BOX structure [Direct3D 10]","a02d025c-3b75-5cb1-2b68-a6c9d6261bf1","d3d10/D3D10_BOX","direct3d10.d3d10_box"]
old-location: direct3d10\d3d10_box.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_box.htm
ms.date: 12/05/2018
ms.keywords: D3D10_BOX, D3D10_BOX structure [Direct3D 10], a02d025c-3b75-5cb1-2b68-a6c9d6261bf1, d3d10/D3D10_BOX, direct3d10.d3d10_box
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
req.typenames: D3D10_BOX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BOX
 - d3d10/D3D10_BOX
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
 - D3D10_BOX
---

# D3D10_BOX structure


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

<img alt="Diagram of a 3D box, where the origin is the left, front, top corner" src="./images/d3d10_box.png"/>

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
