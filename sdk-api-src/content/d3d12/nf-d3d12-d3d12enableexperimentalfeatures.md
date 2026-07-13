---
UID: NF:d3d12.D3D12EnableExperimentalFeatures
title: D3D12EnableExperimentalFeatures function (d3d12.h)
description: Enables a list of experimental features.
helpviewer_keywords: ["D3D12EnableExperimentalFeatures","D3D12EnableExperimentalFeatures function","d3d12/D3D12EnableExperimentalFeatures","direct3d12.d3d12enableexperimentalfeatures"]
old-location: direct3d12\d3d12enableexperimentalfeatures.htm
tech.root: direct3d12
ms.assetid: 290E147E-8545-4572-BB36-58481065C541
ms.date: 08/10/2022
ms.keywords: D3D12EnableExperimentalFeatures, D3D12EnableExperimentalFeatures function, d3d12/D3D12EnableExperimentalFeatures, direct3d12.d3d12enableexperimentalfeatures
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12EnableExperimentalFeatures
 - d3d12/D3D12EnableExperimentalFeatures
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12EnableExperimentalFeatures
---

# D3D12EnableExperimentalFeatures function


## -description

Enables a list of experimental features.

## -parameters

### -param NumFeatures

Type: <b>UINT</b>

The number of experimental features to enable.

### -param pIIDs [in]

Type: <b>const IID*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values?view=vs-2015&preserve-view=true">SAL</a>: <code>__in_ecount(NumFeatures)</code>

A pointer to an array of IDs that specify which of the available experimental features to enable.

### -param pConfigurationStructs [in]

Type: <b>void*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values?view=vs-2015&preserve-view=true">SAL</a>: <code>__in_ecount(NumFeatures)</code>

Structures that contain additional configuration details that some experimental features might need to be enabled.

### -param pConfigurationStructSizes [in]

Type: <b>UINT*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values?view=vs-2015&preserve-view=true">SAL</a>: <code>__in_ecount(NumFeatures)</code>

The sizes of any configuration structs passed in pConfigurationStructs parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code that can include E_NOINTERFACE if an unrecognized feature is specified or Developer Mode is not enabled, or E_INVALIDARG if the configuration of a feature is in correct, the experimental features specified are not compatible, or other errors.

## -remarks

Call this function before device creation.

Because the set of experimental features will change over time, and because these features may not be stable, they are intended for development and experimentation only. This is enforced by requiring Developer Mode to be active before any experimental features can be enabled.

The set of experimental features that are currently supported can be found in the D3D12.h header, near the definition of the D3D12EnableExperimentalFeatures function; because experimental features are only made available infrequently, its typical to find that no experimental features are currently supported.

Some experimental features might be identified by using an IID as the GUID. For these features, you can use D3D12GetDebugInterface, passing an IID as a parameter, to retrieve the interface for manipulating that feature.

If this function is called again with a different list of features to enable, all current D3D12 devices are set to the DEVICE_REMOVED state.


#### Examples

This example shows what an experimental feature definition looks like.


```cpp
// --------------------------------------------------------------------------------------------------------------------------------
// Experimental Feature: D3D12ExperimentalShaderModels
//
// Use with D3D12EnableExperimentalFeatures to enable experimental shader model support,
// meaning shader models that haven't been finalized for use in retail.
//
// Enabling D3D12ExperimentalShaderModels needs no configuration struct, pass NULL in the pConfigurationStructs array.
//
// --------------------------------------------------------------------------------------------------------------------------------
static const UUID D3D12ExperimentalShaderModels = { /* 76f5573e-f13a-40f5-b297-81ce9e18933f */
    0x76f5573e,
    0xf13a,
    0x40f5,
    { 0xb2, 0x97, 0x81, 0xce, 0x9e, 0x18, 0x93, 0x3f }
};
	
```

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-functions">Core Functions</a>