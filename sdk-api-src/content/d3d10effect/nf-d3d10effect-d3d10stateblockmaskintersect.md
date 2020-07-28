---
UID: NF:d3d10effect.D3D10StateBlockMaskIntersect
title: D3D10StateBlockMaskIntersect function (d3d10effect.h)
description: Combine two state-block masks with a bitwise AND.
helpviewer_keywords: ["7ef37c3a-8924-5736-9b40-6a56cdf480c7","D3D10StateBlockMaskIntersect","D3D10StateBlockMaskIntersect function [Direct3D 10]","d3d10effect/D3D10StateBlockMaskIntersect","direct3d10.d3d10stateblockmaskintersect"]
old-location: direct3d10\d3d10stateblockmaskintersect.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskintersect.htm
ms.date: 12/05/2018
ms.keywords: 7ef37c3a-8924-5736-9b40-6a56cdf480c7, D3D10StateBlockMaskIntersect, D3D10StateBlockMaskIntersect function [Direct3D 10], d3d10effect/D3D10StateBlockMaskIntersect, direct3d10.d3d10stateblockmaskintersect
f1_keywords:
- d3d10effect/D3D10StateBlockMaskIntersect
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- D3D10.dll
api_name:
- D3D10StateBlockMaskIntersect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# D3D10StateBlockMaskIntersect function


## -description


Combine two state-block masks with a bitwise AND.


## -parameters




### -param pA [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the left side of the bitwise AND operation. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>.


### -param pB [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask on the right side of the bitwise AND operation.


### -param pResult [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

The result of the bitwise AND operation.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions</a>
 

 

