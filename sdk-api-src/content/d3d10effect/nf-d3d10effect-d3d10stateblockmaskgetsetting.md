---
UID: NF:d3d10effect.D3D10StateBlockMaskGetSetting
title: D3D10StateBlockMaskGetSetting function (d3d10effect.h)
description: Get an element in a state-block mask; determine if an element is allowed by the mask for capturing and applying.
helpviewer_keywords: ["6309c42d-db39-eb28-25e5-ba740c57a969","D3D10StateBlockMaskGetSetting","D3D10StateBlockMaskGetSetting function [Direct3D 10]","d3d10effect/D3D10StateBlockMaskGetSetting","direct3d10.d3d10stateblockmaskgetsetting"]
old-location: direct3d10\d3d10stateblockmaskgetsetting.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskgetsetting.htm
ms.date: 12/05/2018
ms.keywords: 6309c42d-db39-eb28-25e5-ba740c57a969, D3D10StateBlockMaskGetSetting, D3D10StateBlockMaskGetSetting function [Direct3D 10], d3d10effect/D3D10StateBlockMaskGetSetting, direct3d10.d3d10stateblockmaskgetsetting
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
 - D3D10StateBlockMaskGetSetting
 - d3d10effect/D3D10StateBlockMaskGetSetting
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
 - D3D10StateBlockMaskGetSetting
---

# D3D10StateBlockMaskGetSetting function


## -description

Get an element in a state-block mask; determine if an element is allowed by the mask for capturing and applying.

## -parameters

### -param pMask [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask. See <a href="/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask">D3D10_STATE_BLOCK_MASK</a>.

### -param StateType [in]

Type: <b><a href="/windows/desktop/api/d3d10effect/ne-d3d10effect-d3d10_device_state_types">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state. See <a href="/windows/desktop/api/d3d10effect/ne-d3d10effect-d3d10_device_state_types">D3D10_DEVICE_STATE_TYPES</a>.

### -param Entry [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The entry within the device state. This is only relevant for state types that have more than one entry, such as D3D10_DST_GS_SAMPLERS.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns true if the specified feature is allowed by the mask for capturing and applying, and false otherwise.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-effect-functions">Effect Functions</a>