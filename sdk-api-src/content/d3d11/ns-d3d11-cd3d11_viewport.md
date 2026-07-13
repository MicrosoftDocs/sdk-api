---
UID: NS:d3d11.CD3D11_VIEWPORT
title: CD3D11_VIEWPORT (d3d11.h)
description: Represents a viewport and provides convenience methods for creating viewports.
helpviewer_keywords: ["CD3D11_VIEWPORT","CD3D11_VIEWPORT structure [Direct3D 11]","d3d11/CD3D11_VIEWPORT","direct3d11.cd3d11_viewport"]
old-location: direct3d11\cd3d11_viewport.htm
tech.root: direct3d11
ms.assetid: F4C7E5E7-1986-4210-83BC-80277A47CB97
ms.date: 12/05/2018
ms.keywords: CD3D11_VIEWPORT, CD3D11_VIEWPORT structure [Direct3D 11], d3d11/CD3D11_VIEWPORT, direct3d11.cd3d11_viewport
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
 - CD3D11_VIEWPORT
 - d3d11/CD3D11_VIEWPORT
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
 - CD3D11_VIEWPORT
---

# CD3D11_VIEWPORT structure


## -description

Represents a viewport and provides convenience methods for creating viewports.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_VIEWPORT</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_VIEWPORT : public D3D11_VIEWPORT
{
    CD3D11_VIEWPORT()
    {}
    explicit CD3D11_VIEWPORT( const D3D11_VIEWPORT&amp; o ) :
        D3D11_VIEWPORT( o )
    {}
    explicit CD3D11_VIEWPORT(
        FLOAT topLeftX,
        FLOAT topLeftY,
        FLOAT width,
        FLOAT height,
        FLOAT minDepth = D3D11_MIN_DEPTH,
        FLOAT maxDepth = D3D11_MAX_DEPTH )
    {
        TopLeftX = topLeftX;
        TopLeftY = topLeftY;
        Width = width;
        Height = height;
        MinDepth = minDepth;
        MaxDepth = maxDepth;
    }
    explicit CD3D11_VIEWPORT(
        _In_ ID3D11Buffer*,
        _In_ ID3D11RenderTargetView* pRTView,
        FLOAT topLeftX = 0.0f,
        FLOAT minDepth = D3D11_MIN_DEPTH,
        FLOAT maxDepth = D3D11_MAX_DEPTH )
    {
        D3D11_RENDER_TARGET_VIEW_DESC RTVDesc;
        pRTView-&gt;GetDesc( &amp;RTVDesc );
        UINT NumElements = 0;
        switch (RTVDesc.ViewDimension)
        {
        case D3D11_RTV_DIMENSION_BUFFER:
            NumElements = RTVDesc.Buffer.NumElements;
            break;
        default: break;
        }
        TopLeftX = topLeftX;
        TopLeftY = 0.0f;
        Width = NumElements - topLeftX;
        Height = 1.0f;
        MinDepth = minDepth;
        MaxDepth = maxDepth;
    }
    explicit CD3D11_VIEWPORT(
        _In_ ID3D11Texture1D* pTex1D,
        _In_ ID3D11RenderTargetView* pRTView,
        FLOAT topLeftX = 0.0f,
        FLOAT minDepth = D3D11_MIN_DEPTH,
        FLOAT maxDepth = D3D11_MAX_DEPTH )
    {
        D3D11_TEXTURE1D_DESC TexDesc;
        pTex1D-&gt;GetDesc( &amp;TexDesc );
        D3D11_RENDER_TARGET_VIEW_DESC RTVDesc;
        pRTView-&gt;GetDesc( &amp;RTVDesc );
        UINT MipSlice = 0;
        switch (RTVDesc.ViewDimension)
        {
        case D3D11_RTV_DIMENSION_TEXTURE1D:
            MipSlice = RTVDesc.Texture1D.MipSlice;
            break;
        case D3D11_RTV_DIMENSION_TEXTURE1DARRAY:
            MipSlice = RTVDesc.Texture1DArray.MipSlice;
            break;
        default: break;
        }
        const UINT SubResourceWidth = TexDesc.Width / (UINT( 1 ) &lt;&lt; MipSlice);
        TopLeftX = topLeftX;
        TopLeftY = 0.0f;
        Width = (SubResourceWidth ? SubResourceWidth : 1) - topLeftX;
        Height = 1.0f;
        MinDepth = minDepth;
        MaxDepth = maxDepth;
    }
    explicit CD3D11_VIEWPORT(
        _In_ ID3D11Texture2D* pTex2D,
        _In_ ID3D11RenderTargetView* pRTView,
        FLOAT topLeftX = 0.0f,
        FLOAT topLeftY = 0.0f,
        FLOAT minDepth = D3D11_MIN_DEPTH,
        FLOAT maxDepth = D3D11_MAX_DEPTH )
    {
        D3D11_TEXTURE2D_DESC TexDesc;
        pTex2D-&gt;GetDesc( &amp;TexDesc );
        D3D11_RENDER_TARGET_VIEW_DESC RTVDesc;
        pRTView-&gt;GetDesc( &amp;RTVDesc );
        UINT MipSlice = 0;
        switch (RTVDesc.ViewDimension)
        {
        case D3D11_RTV_DIMENSION_TEXTURE2D:
            MipSlice = RTVDesc.Texture2D.MipSlice;
            break;
        case D3D11_RTV_DIMENSION_TEXTURE2DARRAY:
            MipSlice = RTVDesc.Texture2DArray.MipSlice;
            break;
        case D3D11_RTV_DIMENSION_TEXTURE2DMS:
        case D3D11_RTV_DIMENSION_TEXTURE2DMSARRAY:
            break;
        default: break;
        }
        const UINT SubResourceWidth = TexDesc.Width / (UINT( 1 ) &lt;&lt; MipSlice);
        const UINT SubResourceHeight = TexDesc.Height / (UINT( 1 ) &lt;&lt; MipSlice);
        TopLeftX = topLeftX;
        TopLeftY = topLeftY;
        Width = (SubResourceWidth ? SubResourceWidth : 1) - topLeftX;
        Height = (SubResourceHeight ? SubResourceHeight : 1) - topLeftY;
        MinDepth = minDepth;
        MaxDepth = maxDepth;
    }
    explicit CD3D11_VIEWPORT(
        _In_ ID3D11Texture3D* pTex3D,
        _In_ ID3D11RenderTargetView* pRTView,
        FLOAT topLeftX = 0.0f,
        FLOAT topLeftY = 0.0f,
        FLOAT minDepth = D3D11_MIN_DEPTH,
        FLOAT maxDepth = D3D11_MAX_DEPTH )
    {
        D3D11_TEXTURE3D_DESC TexDesc;
        pTex3D-&gt;GetDesc( &amp;TexDesc );
        D3D11_RENDER_TARGET_VIEW_DESC RTVDesc;
        pRTView-&gt;GetDesc( &amp;RTVDesc );
        UINT MipSlice = 0;
        switch (RTVDesc.ViewDimension)
        {
        case D3D11_RTV_DIMENSION_TEXTURE3D:
            MipSlice = RTVDesc.Texture3D.MipSlice;
            break;
        default: break;
        }
        const UINT SubResourceWidth = TexDesc.Width / (UINT( 1 ) &lt;&lt; MipSlice);
        const UINT SubResourceHeight = TexDesc.Height / (UINT( 1 ) &lt;&lt; MipSlice);
        TopLeftX = topLeftX;
        TopLeftY = topLeftY;
        Width = (SubResourceWidth ? SubResourceWidth : 1) - topLeftX;
        Height = (SubResourceHeight ? SubResourceHeight : 1) - topLeftY;
        MinDepth = minDepth;
        MaxDepth = maxDepth;
    }
    ~CD3D11_VIEWPORT() {}
    operator const D3D11_VIEWPORT&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>