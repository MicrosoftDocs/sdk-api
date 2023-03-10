---
UID: NF:d3d10effect.D3D10StateBlockMaskUnion
title: D3D10StateBlockMaskUnion function (d3d10effect.h)
description: Combine two state-block masks with a bitwise OR.
helpviewer_keywords: ["D3D10StateBlockMaskUnion","D3D10StateBlockMaskUnion function [Direct3D 10]","c41aabcb-aa6c-e4b6-5de4-b68cb7241686","d3d10effect/D3D10StateBlockMaskUnion","direct3d10.d3d10stateblockmaskunion"]
old-location: direct3d10\d3d10stateblockmaskunion.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskunion.htm
ms.date: 12/05/2018
ms.keywords: D3D10StateBlockMaskUnion, D3D10StateBlockMaskUnion function [Direct3D 10], c41aabcb-aa6c-e4b6-5de4-b68cb7241686, d3d10effect/D3D10StateBlockMaskUnion, direct3d10.d3d10stateblockmaskunion
req.header: d3d10effect.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10StateBlockMaskUnion
 - d3d10effect/D3D10StateBlockMaskUnion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10StateBlockMaskUnion
---

# D3D10StateBlockMaskUnion function


## -description

Combine two state-block masks with a bitwise OR.

## -parameters

### -param pA [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the left side of the bitwise OR operation. See <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>.

### -param pB [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the right side of the bitwise OR operation.

### -param pResult [out]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

The result of the bitwise OR operation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions</a>