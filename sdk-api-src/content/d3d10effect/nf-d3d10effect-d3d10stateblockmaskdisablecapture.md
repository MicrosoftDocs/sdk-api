---
UID: NF:d3d10effect.D3D10StateBlockMaskDisableCapture
title: D3D10StateBlockMaskDisableCapture function (d3d10effect.h)
description: Disable state capturing with a state-block mask.
helpviewer_keywords: ["94486a35-b1e6-78b2-b9fb-00c0ab5d19f3","D3D10StateBlockMaskDisableCapture","D3D10StateBlockMaskDisableCapture function [Direct3D 10]","d3d10effect/D3D10StateBlockMaskDisableCapture","direct3d10.d3d10stateblockmaskdisablecapture"]
old-location: direct3d10\d3d10stateblockmaskdisablecapture.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskdisablecapture.htm
ms.date: 12/05/2018
ms.keywords: 94486a35-b1e6-78b2-b9fb-00c0ab5d19f3, D3D10StateBlockMaskDisableCapture, D3D10StateBlockMaskDisableCapture function [Direct3D 10], d3d10effect/D3D10StateBlockMaskDisableCapture, direct3d10.d3d10stateblockmaskdisablecapture
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
 - D3D10StateBlockMaskDisableCapture
 - d3d10effect/D3D10StateBlockMaskDisableCapture
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
 - D3D10StateBlockMaskDisableCapture
---

# D3D10StateBlockMaskDisableCapture function


## -description

Disable state capturing with a state-block mask.

## -parameters

### -param pMask [in, out]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

A state block mask (see <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>).

### -param StateType [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ne-d3d10effect-d3d10_device_state_types">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state to disable (see <a href="/windows/desktop/api/d3d10effect/ne-d3d10effect-d3d10_device_state_types">D3D10_DEVICE_STATE_TYPES</a>).

### -param RangeStart [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The lower end of the range of values to set to false.

### -param RangeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The upper end of the range of values to set to false.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This is an example of how to call this function. It creates a mask that cannot capture and apply to geometry-shader samplers in slots 2 ~ 23.


```

D3D10_STATE_BLOCK_MASK stateBlockMask;
D3D10StateBlockMaskDisableCapture(&stateBlockMask, 
                                 D3D10_DST_GS_SAMPLERS, 
                                 2, 23);

```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions</a>