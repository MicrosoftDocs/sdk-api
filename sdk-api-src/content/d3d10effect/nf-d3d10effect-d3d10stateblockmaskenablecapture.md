---
UID: NF:d3d10effect.D3D10StateBlockMaskEnableCapture
title: D3D10StateBlockMaskEnableCapture function (d3d10effect.h)
description: Enable a range of state values in a state block mask.
helpviewer_keywords: ["D3D10StateBlockMaskEnableCapture","D3D10StateBlockMaskEnableCapture function [Direct3D 10]","d3d10effect/D3D10StateBlockMaskEnableCapture","direct3d10.d3d10stateblockmaskenablecapture","facce8d7-c03d-439b-89fb-733b2d013965"]
old-location: direct3d10\d3d10stateblockmaskenablecapture.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskenablecapture.htm
ms.date: 12/05/2018
ms.keywords: D3D10StateBlockMaskEnableCapture, D3D10StateBlockMaskEnableCapture function [Direct3D 10], d3d10effect/D3D10StateBlockMaskEnableCapture, direct3d10.d3d10stateblockmaskenablecapture, facce8d7-c03d-439b-89fb-733b2d013965
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
 - D3D10StateBlockMaskEnableCapture
 - d3d10effect/D3D10StateBlockMaskEnableCapture
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
 - D3D10StateBlockMaskEnableCapture
---

# D3D10StateBlockMaskEnableCapture function


## -description

Enable a range of state values in a state block mask.

## -parameters

### -param pMask [in, out]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

A state block mask (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>).

### -param StateType [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ne-d3d10effect-d3d10_device_state_types">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state to enable (see <a href="/windows/desktop/api/d3d10effect/ne-d3d10effect-d3d10_device_state_types">D3D10_DEVICE_STATE_TYPES</a>.

### -param RangeStart [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The lower end of the range of values to set to true.

### -param RangeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The upper end of the range of values to set to true.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This is an example of how to call this function. It create a mask that can capture and apply to geometry-shader samplers in slots 2 ~ 13.


```

D3D10_STATE_BLOCK_MASK stateBlockMask;
D3D10StateBlockMaskEnableCapture(&stateBlockMask, 
                                 D3D10_DST_GS_SAMPLERS, 
                                 2, 13);

```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions</a>