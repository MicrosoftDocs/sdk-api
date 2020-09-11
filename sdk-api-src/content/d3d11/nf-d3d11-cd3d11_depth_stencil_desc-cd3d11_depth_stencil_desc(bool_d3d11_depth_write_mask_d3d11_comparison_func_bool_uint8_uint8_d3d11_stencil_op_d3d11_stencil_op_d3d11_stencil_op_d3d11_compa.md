---
UID: NF:d3d11.CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC(BOOL,D3D11_DEPTH_WRITE_MASK,D3D11_COMPARISON_FUNC,BOOL,UINT8,UINT8,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_COMPA
title: CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(BOOL,D3D11_DEPTH_WRITE_MASK,D3D11_COMPARISON_FUNC,BOOL,UINT8,UINT8,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_COMPA (d3d11.h)
description: Instantiates a new instance of a CD3D11_DEPTH_STENCIL_DESC structure that is initialized with D3D11_DEPTH_STENCIL_DESC values.
helpviewer_keywords: ["CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11]","CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11]","CD3D11_DEPTH_STENCIL_DESC interface","CD3D11_DEPTH_STENCIL_DESC interface [Direct3D 11]","CD3D11_DEPTH_STENCIL_DESC constructor","CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC(BOOL","D3D11_DEPTH_WRITE_MASK","D3D11_COMPARISON_FUNC","BOOL","UINT8","UINT8","D3D11_STENCIL_OP","D3D11_STENCIL_OP","D3D11_STENCIL_OP","D3D11_COMPA","CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC()","CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(BOOL","D3D11_DEPTH_WRITE_MASK","D3D11_COMPARISON_FUNC","BOOL","UINT8","UINT8","D3D11_STENCIL_OP","D3D11_STENCIL_OP","D3D11_STENCIL_OP","D3D11_COMPA","d3d11/CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC","direct3d11.cd3d11_depth_stencil_desc_cd3d11_depth_stencil_desc"]
old-location: 
tech.root: direct3d11
ms.assetid: 9AB17F96-B5BB-4A6B-94E2-F68ADC27B3C2
ms.date: 05/06/2019
ms.keywords: CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11], CD3D11_DEPTH_STENCIL_DESC constructor [Direct3D 11],CD3D11_DEPTH_STENCIL_DESC interface, CD3D11_DEPTH_STENCIL_DESC interface [Direct3D 11],CD3D11_DEPTH_STENCIL_DESC constructor, CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC(BOOL,D3D11_DEPTH_WRITE_MASK,D3D11_COMPARISON_FUNC,BOOL,UINT8,UINT8,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_COMPA, CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(), CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(BOOL,D3D11_DEPTH_WRITE_MASK,D3D11_COMPARISON_FUNC,BOOL,UINT8,UINT8,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_COMPA, d3d11/CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC, direct3d11.cd3d11_depth_stencil_desc_cd3d11_depth_stencil_desc
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC
 - d3d11/CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - CD3D11_DEPTH_STENCIL_DESC.CD3D11_DEPTH_STENCIL_DESC
---

# CD3D11_DEPTH_STENCIL_DESC::CD3D11_DEPTH_STENCIL_DESC(BOOL,D3D11_DEPTH_WRITE_MASK,D3D11_COMPARISON_FUNC,BOOL,UINT8,UINT8,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_STENCIL_OP,D3D11_COMPA


## -description

Instantiates a new instance of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/jj151632(v=vs.85)">CD3D11_DEPTH_STENCIL_DESC</a> structure that is initialized with <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a> values.

## -parameters

### -param depthEnable

A Boolean value that specifies whether to enable depth testing (**TRUE** for enabled, **FALSE** for disabled).

### -param depthWriteMask

A **D3D11_DEPTH_WRITE_MASK**-typed value that identifies a portion of the depth-stencil buffer that can be modified by depth data.

### -param depthFunc

A **D3D11_COMPARISON_FUNC**-typed value that identifies a function that compares depth data against existing depth data.

### -param stencilEnable

A Boolean value that specifies whether to enable stencil testing (**TRUE** for enabled, **FALSE** for disabled).

### -param stencilReadMask

An 8-bit mask that identifies a portion of the depth-stencil buffer for reading stencil data.

### -param stencilWriteMask

An 8-bit mask that identifies a portion of the depth-stencil buffer for writing stencil data.

### -param frontStencilFailOp

A **D3D11_STENCIL_OP**-typed value that identifies the stencil operation to perform when stencil testing fails for pixels whose surface normal is facing towards the camera.

### -param frontStencilDepthFailOp

A **D3D11_STENCIL_OP**-typed value that identifies the stencil operation to perform when stencil testing passes and depth testing fails for pixels whose surface normal is facing towards the camera.

### -param frontStencilPassOp

A **D3D11_STENCIL_OP**-typed value that identifies the stencil operation to perform when stencil testing and depth testing both pass for pixels whose surface normal is facing towards the camera.

### -param frontStencilFunc

A **D3D11_COMPARISON_FUNC**-typed value that identifies a function that compares stencil data against existing stencil data for pixels whose surface normal is facing towards the camera.

### -param backStencilFailOp

A **D3D11_STENCIL_OP**-typed value that identifies the stencil operation to perform when stencil testing fails for pixels whose surface normal is facing away from the camera.

### -param backStencilDepthFailOp

A **D3D11_STENCIL_OP**-typed value that identifies the stencil operation to perform when stencil testing passes and depth testing fails for pixels whose surface normal is facing away from the camera.

### -param backStencilPassOp

A **D3D11_STENCIL_OP**-typed value that identifies the stencil operation to perform when stencil testing and depth testing both pass for pixels whose surface normal is facing away from the camera.

### -param backStencilFunc

A **D3D11_COMPARISON_FUNC**-typed value that identifies a function that compares stencil data against existing stencil data for pixels whose surface normal is facing away from the camera.

## -remarks

Here is how **CD3D11_DEPTH_STENCIL_DESC** assigns the provided values to the members of **D3D11_DEPTH_STENCIL_DESC**:

```
        DepthEnable = depthEnable;
        DepthWriteMask = depthWriteMask;
        DepthFunc = depthFunc;
        StencilEnable = stencilEnable;
        StencilReadMask = stencilReadMask;
        StencilWriteMask = stencilWriteMask;
        FrontFace.StencilFailOp = frontStencilFailOp;
        FrontFace.StencilDepthFailOp = frontStencilDepthFailOp;
        FrontFace.StencilPassOp = frontStencilPassOp;
        FrontFace.StencilFunc = frontStencilFunc;
        BackFace.StencilFailOp = backStencilFailOp;
        BackFace.StencilDepthFailOp = backStencilDepthFailOp;
        BackFace.StencilPassOp = backStencilPassOp;
        BackFace.StencilFunc = backStencilFunc;

```

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/jj151632(v=vs.85)">CD3D11_DEPTH_STENCIL_DESC</a>

