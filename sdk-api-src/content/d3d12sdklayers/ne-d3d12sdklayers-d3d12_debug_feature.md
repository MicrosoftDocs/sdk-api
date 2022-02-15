---
UID: NE:d3d12sdklayers.D3D12_DEBUG_FEATURE
title: D3D12_DEBUG_FEATURE (d3d12sdklayers.h)
description: Flags for optional D3D12 Debug Layer features.
helpviewer_keywords: ["D3D12_DEBUG_FEATURE","D3D12_DEBUG_FEATURE enumeration","D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS","D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING","D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION","D3D12_DEBUG_FEATURE_NONE","D3D12_DEBUG_FEATURE_VALID_MASK","d3d12sdklayers/D3D12_DEBUG_FEATURE","d3d12sdklayers/D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS","d3d12sdklayers/D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING","d3d12sdklayers/D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION","d3d12sdklayers/D3D12_DEBUG_FEATURE_NONE","d3d12sdklayers/D3D12_DEBUG_FEATURE_VALID_MASK","direct3d12.d3d12_debug_feature"]
old-location: direct3d12\d3d12_debug_feature.htm
tech.root: direct3d12
ms.assetid: 36E0A5DC-8313-4D9D-988C-21E6FFCC8730
ms.date: 12/05/2018
ms.keywords: D3D12_DEBUG_FEATURE, D3D12_DEBUG_FEATURE enumeration, D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS, D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING, D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION, D3D12_DEBUG_FEATURE_NONE, D3D12_DEBUG_FEATURE_VALID_MASK, d3d12sdklayers/D3D12_DEBUG_FEATURE, d3d12sdklayers/D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS, d3d12sdklayers/D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING, d3d12sdklayers/D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION, d3d12sdklayers/D3D12_DEBUG_FEATURE_NONE, d3d12sdklayers/D3D12_DEBUG_FEATURE_VALID_MASK, direct3d12.d3d12_debug_feature
req.header: d3d12sdklayers.h
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
req.typenames: D3D12_DEBUG_FEATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEBUG_FEATURE
 - d3d12sdklayers/D3D12_DEBUG_FEATURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_DEBUG_FEATURE
---

# D3D12_DEBUG_FEATURE enumeration


## -description

Flags for optional D3D12 Debug Layer features.

## -enum-fields

### -field D3D12_DEBUG_FEATURE_NONE:0

The default. No optional Debug Layer features.

### -field D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS:0x1

The Debug Layer is allowed to deliberately change functional behavior of an application in order to help identify potential errors.  By default, the Debug Layer allows most invalid API usage to run the natural course.

### -field D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING:0x2

Performs additional resource state validation of resources set in descriptors at the time <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ID3D12CommandQueue::ExecuteCommandLists</a> is called.  By design descriptors can be changed even after submitting command lists assuming proper synchronization.  Conservative resource state tracking ignores this allowance and validates all resources used in descriptor tables when <b>ExecuteCommandLists</b> is called.  The result may be false validation errors.

### -field D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION:0x4

Disables validation of bundle commands by virtually injecting checks into the calling command list validation paths.

### -field D3D12_DEBUG_FEATURE_VALID_MASK

Internal use only.

## -remarks

This enum is used by <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter">ID3D12DebugDevice1::SetDebugParameter</a> and <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter">ID3D12DebugDevice1::GetDebugParameter</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-enumerations">Debug Layer Enumerations</a>
