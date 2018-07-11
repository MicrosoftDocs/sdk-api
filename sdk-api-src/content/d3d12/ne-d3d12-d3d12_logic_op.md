---
UID: NE:d3d12.D3D12_LOGIC_OP
title: D3D12_LOGIC_OP
author: windows-sdk-content
description: Specifies logical operations to configure for a render target.
old-location: direct3d12\d3d12_logic_op.htm
old-project: direct3d12
ms.assetid: 4F6BBCA8-6CF1-42BD-8B05-CD6D285CDFBF
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: D3D12_LOGIC_OP, D3D12_LOGIC_OP enumeration, D3D12_LOGIC_OP_AND, D3D12_LOGIC_OP_AND_INVERTED, D3D12_LOGIC_OP_AND_REVERSE, D3D12_LOGIC_OP_CLEAR, D3D12_LOGIC_OP_COPY, D3D12_LOGIC_OP_COPY_INVERTED, D3D12_LOGIC_OP_EQUIV, D3D12_LOGIC_OP_INVERT, D3D12_LOGIC_OP_NAND, D3D12_LOGIC_OP_NOOP, D3D12_LOGIC_OP_NOR, D3D12_LOGIC_OP_OR, D3D12_LOGIC_OP_OR_INVERTED, D3D12_LOGIC_OP_OR_REVERSE, D3D12_LOGIC_OP_SET, D3D12_LOGIC_OP_XOR, d3d12/D3D12_LOGIC_OP, d3d12/D3D12_LOGIC_OP_AND, d3d12/D3D12_LOGIC_OP_AND_INVERTED, d3d12/D3D12_LOGIC_OP_AND_REVERSE, d3d12/D3D12_LOGIC_OP_CLEAR, d3d12/D3D12_LOGIC_OP_COPY, d3d12/D3D12_LOGIC_OP_COPY_INVERTED, d3d12/D3D12_LOGIC_OP_EQUIV, d3d12/D3D12_LOGIC_OP_INVERT, d3d12/D3D12_LOGIC_OP_NAND, d3d12/D3D12_LOGIC_OP_NOOP, d3d12/D3D12_LOGIC_OP_NOR, d3d12/D3D12_LOGIC_OP_OR, d3d12/D3D12_LOGIC_OP_OR_INVERTED, d3d12/D3D12_LOGIC_OP_OR_REVERSE, d3d12/D3D12_LOGIC_OP_SET, d3d12/D3D12_LOGIC_OP_XOR, direct3d12.d3d12_logic_op
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
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
tech.root: 
req.typenames: D3D12_LOGIC_OP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_LOGIC_OP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_LOGIC_OP enumeration


## -description


Specifies logical operations to configure for a render target.


## -enum-fields




### -field D3D12_LOGIC_OP_CLEAR

Clears the render target.


### -field D3D12_LOGIC_OP_SET

Sets the render target.


### -field D3D12_LOGIC_OP_COPY

Copys the render target.


### -field D3D12_LOGIC_OP_COPY_INVERTED

Performs an inverted-copy of the render target.


### -field D3D12_LOGIC_OP_NOOP

No operation is performed on the render target.


### -field D3D12_LOGIC_OP_INVERT

Inverts the render target.


### -field D3D12_LOGIC_OP_AND

Performs a logical AND operation on the render target.


### -field D3D12_LOGIC_OP_NAND

Performs a logical NAND operation on the render target.


### -field D3D12_LOGIC_OP_OR

Performs a logical OR operation on the render target.


### -field D3D12_LOGIC_OP_NOR

Performs a logical NOR operation on the render target.


### -field D3D12_LOGIC_OP_XOR

Performs a logical XOR operation on the render target.


### -field D3D12_LOGIC_OP_EQUIV

Performs a logical equal operation on the render target.


### -field D3D12_LOGIC_OP_AND_REVERSE

Performs a logical AND and reverse operation on the render target.


### -field D3D12_LOGIC_OP_AND_INVERTED

Performs a logical AND and invert operation on the render target.


### -field D3D12_LOGIC_OP_OR_REVERSE

Performs a logical OR and reverse operation on the render target.


### -field D3D12_LOGIC_OP_OR_INVERTED

Performs a logical OR and invert operation on the render target.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/911158CF-5F4F-4211-8CC6-F73BDB697BC5">D3D12_RENDER_TARGET_BLEND_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

