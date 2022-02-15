---
UID: NE:d3d11_1.D3D11_LOGIC_OP
title: D3D11_LOGIC_OP (d3d11_1.h)
description: Specifies logical operations to configure for a render target.
helpviewer_keywords: ["D3D11_LOGIC_OP","D3D11_LOGIC_OP enumeration [Direct3D 11]","D3D11_LOGIC_OP_AND","D3D11_LOGIC_OP_AND_INVERTED","D3D11_LOGIC_OP_AND_REVERSE","D3D11_LOGIC_OP_CLEAR","D3D11_LOGIC_OP_COPY","D3D11_LOGIC_OP_COPY_INVERTED","D3D11_LOGIC_OP_EQUIV","D3D11_LOGIC_OP_INVERT","D3D11_LOGIC_OP_NAND","D3D11_LOGIC_OP_NOOP","D3D11_LOGIC_OP_NOR","D3D11_LOGIC_OP_OR","D3D11_LOGIC_OP_OR_INVERTED","D3D11_LOGIC_OP_OR_REVERSE","D3D11_LOGIC_OP_SET","D3D11_LOGIC_OP_XOR","d3d11_1/D3D11_LOGIC_OP","d3d11_1/D3D11_LOGIC_OP_AND","d3d11_1/D3D11_LOGIC_OP_AND_INVERTED","d3d11_1/D3D11_LOGIC_OP_AND_REVERSE","d3d11_1/D3D11_LOGIC_OP_CLEAR","d3d11_1/D3D11_LOGIC_OP_COPY","d3d11_1/D3D11_LOGIC_OP_COPY_INVERTED","d3d11_1/D3D11_LOGIC_OP_EQUIV","d3d11_1/D3D11_LOGIC_OP_INVERT","d3d11_1/D3D11_LOGIC_OP_NAND","d3d11_1/D3D11_LOGIC_OP_NOOP","d3d11_1/D3D11_LOGIC_OP_NOR","d3d11_1/D3D11_LOGIC_OP_OR","d3d11_1/D3D11_LOGIC_OP_OR_INVERTED","d3d11_1/D3D11_LOGIC_OP_OR_REVERSE","d3d11_1/D3D11_LOGIC_OP_SET","d3d11_1/D3D11_LOGIC_OP_XOR","direct3d11.d3d11_logic_op"]
old-location: direct3d11\d3d11_logic_op.htm
tech.root: direct3d11
ms.assetid: F35DF88D-03F9-4CDB-AF97-7216786AF338
ms.date: 12/05/2018
ms.keywords: D3D11_LOGIC_OP, D3D11_LOGIC_OP enumeration [Direct3D 11], D3D11_LOGIC_OP_AND, D3D11_LOGIC_OP_AND_INVERTED, D3D11_LOGIC_OP_AND_REVERSE, D3D11_LOGIC_OP_CLEAR, D3D11_LOGIC_OP_COPY, D3D11_LOGIC_OP_COPY_INVERTED, D3D11_LOGIC_OP_EQUIV, D3D11_LOGIC_OP_INVERT, D3D11_LOGIC_OP_NAND, D3D11_LOGIC_OP_NOOP, D3D11_LOGIC_OP_NOR, D3D11_LOGIC_OP_OR, D3D11_LOGIC_OP_OR_INVERTED, D3D11_LOGIC_OP_OR_REVERSE, D3D11_LOGIC_OP_SET, D3D11_LOGIC_OP_XOR, d3d11_1/D3D11_LOGIC_OP, d3d11_1/D3D11_LOGIC_OP_AND, d3d11_1/D3D11_LOGIC_OP_AND_INVERTED, d3d11_1/D3D11_LOGIC_OP_AND_REVERSE, d3d11_1/D3D11_LOGIC_OP_CLEAR, d3d11_1/D3D11_LOGIC_OP_COPY, d3d11_1/D3D11_LOGIC_OP_COPY_INVERTED, d3d11_1/D3D11_LOGIC_OP_EQUIV, d3d11_1/D3D11_LOGIC_OP_INVERT, d3d11_1/D3D11_LOGIC_OP_NAND, d3d11_1/D3D11_LOGIC_OP_NOOP, d3d11_1/D3D11_LOGIC_OP_NOR, d3d11_1/D3D11_LOGIC_OP_OR, d3d11_1/D3D11_LOGIC_OP_OR_INVERTED, d3d11_1/D3D11_LOGIC_OP_OR_REVERSE, d3d11_1/D3D11_LOGIC_OP_SET, d3d11_1/D3D11_LOGIC_OP_XOR, direct3d11.d3d11_logic_op
req.header: d3d11_1.h
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
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_LOGIC_OP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_LOGIC_OP
 - d3d11_1/D3D11_LOGIC_OP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_1.h
api_name:
 - D3D11_LOGIC_OP
---

# D3D11_LOGIC_OP enumeration


## -description

<div class="alert"><b>Note</b>  This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Specifies logical operations to configure for a render target.

## -enum-fields

### -field D3D11_LOGIC_OP_CLEAR:0

Clears the render target.

### -field D3D11_LOGIC_OP_SET

Sets the render target.

### -field D3D11_LOGIC_OP_COPY

Copys the render target.

### -field D3D11_LOGIC_OP_COPY_INVERTED

Performs an inverted-copy of the render target.

### -field D3D11_LOGIC_OP_NOOP

No operation is performed on the render target.

### -field D3D11_LOGIC_OP_INVERT

Inverts the render target.

### -field D3D11_LOGIC_OP_AND

Performs a logical AND operation on the render target.

### -field D3D11_LOGIC_OP_NAND

Performs a logical NAND operation on the render target.

### -field D3D11_LOGIC_OP_OR

Performs a logical OR operation on the render target.

### -field D3D11_LOGIC_OP_NOR

Performs a logical NOR operation on the render target.

### -field D3D11_LOGIC_OP_XOR

Performs a logical XOR operation on the render target.

### -field D3D11_LOGIC_OP_EQUIV

Performs a logical equal operation on the render target.

### -field D3D11_LOGIC_OP_AND_REVERSE

Performs a logical AND and reverse operation on the render target.

### -field D3D11_LOGIC_OP_AND_INVERTED

Performs a logical AND and invert operation on the render target.

### -field D3D11_LOGIC_OP_OR_REVERSE

Performs a logical OR and reverse operation on the render target.

### -field D3D11_LOGIC_OP_OR_INVERTED

Performs a logical OR and invert operation on the render target.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
