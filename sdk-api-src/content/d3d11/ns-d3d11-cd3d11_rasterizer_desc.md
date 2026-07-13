---
UID: NS:d3d11.CD3D11_RASTERIZER_DESC
title: CD3D11_RASTERIZER_DESC (d3d11.h)
description: Represents a rasterizer-state structure and provides convenience methods for creating rasterizer-state structures.
helpviewer_keywords: ["CD3D11_RASTERIZER_DESC","CD3D11_RASTERIZER_DESC structure [Direct3D 11]","d3d11/CD3D11_RASTERIZER_DESC","direct3d11.cd3d11_rasterizer_desc"]
old-location: direct3d11\cd3d11_rasterizer_desc.htm
tech.root: direct3d11
ms.assetid: 3A64A02B-9DF6-46D1-8695-9B92F25CE620
ms.date: 12/05/2018
ms.keywords: CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC structure [Direct3D 11], d3d11/CD3D11_RASTERIZER_DESC, direct3d11.cd3d11_rasterizer_desc
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
 - CD3D11_RASTERIZER_DESC
 - d3d11/CD3D11_RASTERIZER_DESC
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
 - CD3D11_RASTERIZER_DESC
---

# CD3D11_RASTERIZER_DESC structure


## -description

Represents a rasterizer-state structure and provides convenience methods for creating rasterizer-state structures.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_RASTERIZER_DESC</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_RASTERIZER_DESC : public D3D11_RASTERIZER_DESC
{
    CD3D11_RASTERIZER_DESC()
    {}
    explicit CD3D11_RASTERIZER_DESC( const D3D11_RASTERIZER_DESC&amp; o ) :
        D3D11_RASTERIZER_DESC( o )
    {}
    explicit CD3D11_RASTERIZER_DESC( CD3D11_DEFAULT )
    {
        FillMode = D3D11_FILL_SOLID;
        CullMode = D3D11_CULL_BACK;
        FrontCounterClockwise = FALSE;
        DepthBias = D3D11_DEFAULT_DEPTH_BIAS;
        DepthBiasClamp = D3D11_DEFAULT_DEPTH_BIAS_CLAMP;
        SlopeScaledDepthBias = D3D11_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;
        DepthClipEnable = TRUE;
        ScissorEnable = FALSE;
        MultisampleEnable = FALSE;
        AntialiasedLineEnable = FALSE;
    }
    explicit CD3D11_RASTERIZER_DESC(
        D3D11_FILL_MODE fillMode,
        D3D11_CULL_MODE cullMode,
        BOOL frontCounterClockwise,
        INT depthBias,
        FLOAT depthBiasClamp,
        FLOAT slopeScaledDepthBias,
        BOOL depthClipEnable,
        BOOL scissorEnable,
        BOOL multisampleEnable,
        BOOL antialiasedLineEnable )
    {
        FillMode = fillMode;
        CullMode = cullMode;
        FrontCounterClockwise = frontCounterClockwise;
        DepthBias = depthBias;
        DepthBiasClamp = depthBiasClamp;
        SlopeScaledDepthBias = slopeScaledDepthBias;
        DepthClipEnable = depthClipEnable;
        ScissorEnable = scissorEnable;
        MultisampleEnable = multisampleEnable;
        AntialiasedLineEnable = antialiasedLineEnable;
    }
    ~CD3D11_RASTERIZER_DESC() {}
    operator const D3D11_RASTERIZER_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>