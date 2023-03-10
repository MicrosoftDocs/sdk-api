---
UID: NS:d3d11.CD3D11_DEPTH_STENCIL_DESC
title: CD3D11_DEPTH_STENCIL_DESC (d3d11.h)
description: Represents a depth-stencil-state structure and provides convenience methods for creating depth-stencil-state structures.
helpviewer_keywords: ["CD3D11_DEPTH_STENCIL_DESC","CD3D11_DEPTH_STENCIL_DESC structure [Direct3D 11]","d3d11/CD3D11_DEPTH_STENCIL_DESC","direct3d11.cd3d11_depth_stencil_desc"]
old-location: direct3d11\cd3d11_depth_stencil_desc.htm
tech.root: direct3d11
ms.assetid: 511AF313-C692-423B-AD5A-A0A36018572B
ms.date: 12/05/2018
ms.keywords: CD3D11_DEPTH_STENCIL_DESC, CD3D11_DEPTH_STENCIL_DESC structure [Direct3D 11], d3d11/CD3D11_DEPTH_STENCIL_DESC, direct3d11.cd3d11_depth_stencil_desc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_DEPTH_STENCIL_DESC
 - d3d11/CD3D11_DEPTH_STENCIL_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - CD3D11_DEPTH_STENCIL_DESC
---

# CD3D11_DEPTH_STENCIL_DESC structure


## -description

Represents a depth-stencil-state structure and provides convenience methods for creating depth-stencil-state structures.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_DEPTH_STENCIL_DESC</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_DEPTH_STENCIL_DESC : public D3D11_DEPTH_STENCIL_DESC
{
    CD3D11_DEPTH_STENCIL_DESC()
    {}
    explicit CD3D11_DEPTH_STENCIL_DESC( const D3D11_DEPTH_STENCIL_DESC&amp; o ) :
        D3D11_DEPTH_STENCIL_DESC( o )
    {}
    explicit CD3D11_DEPTH_STENCIL_DESC( CD3D11_DEFAULT )
    {
        DepthEnable = TRUE;
        DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
        DepthFunc = D3D11_COMPARISON_LESS;
        StencilEnable = FALSE;
        StencilReadMask = D3D11_DEFAULT_STENCIL_READ_MASK;
        StencilWriteMask = D3D11_DEFAULT_STENCIL_WRITE_MASK;
        const D3D11_DEPTH_STENCILOP_DESC defaultStencilOp =
        { D3D11_STENCIL_OP_KEEP, D3D11_STENCIL_OP_KEEP, D3D11_STENCIL_OP_KEEP, D3D11_COMPARISON_ALWAYS };
        FrontFace = defaultStencilOp;
        BackFace = defaultStencilOp;
    }
    explicit CD3D11_DEPTH_STENCIL_DESC(
        BOOL depthEnable,
        D3D11_DEPTH_WRITE_MASK depthWriteMask,
        D3D11_COMPARISON_FUNC depthFunc,
        BOOL stencilEnable,
        UINT8 stencilReadMask,
        UINT8 stencilWriteMask,
        D3D11_STENCIL_OP frontStencilFailOp,
        D3D11_STENCIL_OP frontStencilDepthFailOp,
        D3D11_STENCIL_OP frontStencilPassOp,
        D3D11_COMPARISON_FUNC frontStencilFunc,
        D3D11_STENCIL_OP backStencilFailOp,
        D3D11_STENCIL_OP backStencilDepthFailOp,
        D3D11_STENCIL_OP backStencilPassOp,
        D3D11_COMPARISON_FUNC backStencilFunc )
    {
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
    }
    ~CD3D11_DEPTH_STENCIL_DESC() {}
    operator const D3D11_DEPTH_STENCIL_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>