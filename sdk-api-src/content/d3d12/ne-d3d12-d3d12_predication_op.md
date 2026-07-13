---
UID: NE:d3d12.D3D12_PREDICATION_OP
title: D3D12_PREDICATION_OP (d3d12.h)
description: Specifies the predication operation to apply.
helpviewer_keywords: ["D3D12_PREDICATION_OP","D3D12_PREDICATION_OP enumeration","D3D12_PREDICATION_OP_EQUAL_ZERO","D3D12_PREDICATION_OP_NOT_EQUAL_ZERO","d3d12/D3D12_PREDICATION_OP","d3d12/D3D12_PREDICATION_OP_EQUAL_ZERO","d3d12/D3D12_PREDICATION_OP_NOT_EQUAL_ZERO","direct3d12.d3d12_predication_op"]
old-location: direct3d12\d3d12_predication_op.htm
tech.root: direct3d12
ms.assetid: 2A650FE4-7D24-4852-9435-7C3CB73848AB
ms.date: 12/05/2018
ms.keywords: D3D12_PREDICATION_OP, D3D12_PREDICATION_OP enumeration, D3D12_PREDICATION_OP_EQUAL_ZERO, D3D12_PREDICATION_OP_NOT_EQUAL_ZERO, d3d12/D3D12_PREDICATION_OP, d3d12/D3D12_PREDICATION_OP_EQUAL_ZERO, d3d12/D3D12_PREDICATION_OP_NOT_EQUAL_ZERO, direct3d12.d3d12_predication_op
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_PREDICATION_OP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_PREDICATION_OP
 - d3d12/D3D12_PREDICATION_OP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_PREDICATION_OP
---

# D3D12_PREDICATION_OP enumeration


## -description

Specifies the predication operation to apply.

## -enum-fields

### -field D3D12_PREDICATION_OP_EQUAL_ZERO:0

Enables predication if all 64-bits are zero.

### -field D3D12_PREDICATION_OP_NOT_EQUAL_ZERO:1

Enables predication if at least one of the 64-bits are not zero.

## -remarks

This enum is used by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication">SetPredication</a>.
        

Predication is decoupled from queries.
          Predication can be set based on the value of 64-bits within a buffer.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="/windows/desktop/direct3d12/predication">Predication</a>
