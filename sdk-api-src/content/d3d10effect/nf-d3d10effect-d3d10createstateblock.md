---
UID: NF:d3d10effect.D3D10CreateStateBlock
title: D3D10CreateStateBlock function (d3d10effect.h)
description: Create a state block.
helpviewer_keywords: ["8f57946f-10b9-397f-8aa5-63df2e9ef7df","D3D10CreateStateBlock","D3D10CreateStateBlock function [Direct3D 10]","d3d10effect/D3D10CreateStateBlock","direct3d10.d3d10createstateblock"]
old-location: direct3d10\d3d10createstateblock.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createstateblock.htm
ms.date: 12/05/2018
ms.keywords: 8f57946f-10b9-397f-8aa5-63df2e9ef7df, D3D10CreateStateBlock, D3D10CreateStateBlock function [Direct3D 10], d3d10effect/D3D10CreateStateBlock, direct3d10.d3d10createstateblock
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
 - D3D10CreateStateBlock
 - d3d10effect/D3D10CreateStateBlock
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
 - D3D10CreateStateBlock
---

# D3D10CreateStateBlock function


## -description

Create a state block.

## -parameters

### -param pDevice [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>*</b>

The device for which the state block will be created.

### -param pStateBlockMask [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

Indicates which parts of the device state will be captured when calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-capture">ID3D10StateBlock::Capture</a> and reapplied when calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-apply">ID3D10StateBlock::Apply</a>. See remarks.

### -param ppStateBlock [out]

Type: <b><a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock">ID3D10StateBlock</a>**</b>

Address of a pointer to the buffer created (see <a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10stateblock">ID3D10StateBlock Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

A state block is a collection of device state, and is used for saving and restoring device state. Use a state-block mask to enable subsets of state for saving and restoring.

The <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a> structure can be filled manually or by using any of the D3D10StateBlockMaskXXX APIs. A state block mask can also be obtained by calling <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effecttechnique-computestateblockmask">ID3D10EffectTechnique::ComputeStateBlockMask</a> or <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-computestateblockmask">ID3D10EffectPass::ComputeStateBlockMask</a>.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

In Direct3D 10, a state block object does not contain any valid information about the state of the device until <a href="/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10stateblock-capture">ID3D10StateBlock::Capture</a> is called. In Direct3D 9, state is saved in a state block object, when it is created.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions</a>